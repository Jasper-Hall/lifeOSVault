# Projects

Multi-step efforts that require sustained work over time.

## Project Structure

### Single File Format

Projects can be single markdown files with embedded Bases views:

```markdown
## 7. Action Handles

### Tasks
![[Project Management.base#Project Tasks]]

### Epics
![[Project Management.base#Project Epics]]
```

### Project Subdirectory Format

For larger projects, use subdirectories:

```
30_Projects/
└── Mutax/
    ├── README.md          # Project overview
    ├── epics/             # Epic files
    ├── stories/           # Story files
    └── tasks/             # Task files
```

## Task Management

### Task Files

Tasks are individual markdown files with **descriptive names** and YAML frontmatter:

**Naming:** Use kebab-case descriptive names (e.g., `research-can-bus-vs-spi-i2c.md`, not `task_001.md`)

```markdown
---
id: task_research-can-bus-vs-spi-i2c
kind: Task
status: pending
priority: high
urgency: short-term
project: Mutax
blocked_by: []
blocks: []
---

# Research CAN bus vs SPI/I2C

## Context
[Why this task exists]

## Notes
[Progress, blockers, decisions]
```

See `.templates/TASK_NAMING_GUIDE.md` for naming conventions.

### Creating Tasks

1. **From Project File**: Click "+ New" in embedded Bases view
2. **From Template**: Use `Task-Template.md` from `.templates/` folder
3. **From Inbox**: Agent creates task files when processing inbox captures

### Task Properties

- **kind**: Task (or Epic, Story, Idea, Bug)
- **status**: Backlog, To Do, In Progress, Review, Completed
- **priority**: High, Medium, Low
- **urgency**: Immediate, Short-term, Long-term, None
- **project**: Link to project file
- **blocked_by**: List of task IDs blocking this task
- **blocks**: List of task IDs this task blocks
- **due**: Due date (optional)
- **source**: Source file (inbox capture, etc.)

## Bases Integration

The `Project Management.base` file indexes all tasks, epics, and stories across all projects, providing:

- **Dynamic Views**: Filtered by project using `this.file`
- **Cross-Project Views**: See all tasks across all projects
- **Priority Views**: NOW, Blocked, Due Soon
- **Visual Organization**: Card views, table views

## Templates

Templates are available in `.templates/`:
- `Project-Template.md` - New project template
- `Epic-Template.md` - Epic template
- `Story-Template.md` - Story template
- `Task-Template.md` - Task template
