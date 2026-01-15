# Task File Naming Guide

## Naming Convention

Task files should be named with **descriptive, kebab-case names** based on the actual task content.

## Examples

✅ **Good Names:**
- `research-can-bus-vs-spi-i2c.md`
- `purchase-tablets-touch-osc.md`
- `complete-firmware-refactoring.md`
- `test-decoupled-firmware-architecture.md`
- `design-pcb-architecture.md`
- `contact-chris-kuscinsky-can-bus.md`

❌ **Bad Names:**
- `task_001.md`
- `task1.md`
- `mutax-task-1.md`
- `Research CAN Bus.md` (spaces, capitals)

## Rules

1. **Use kebab-case**: lowercase with hyphens (e.g., `research-can-bus`)
2. **Be descriptive**: Name should clearly indicate what the task is
3. **Keep it concise**: 3-5 words is usually enough
4. **Use verbs**: Start with action words (research, design, implement, test, etc.)
5. **Include key terms**: Include important nouns (can-bus, tablets, firmware, etc.)

## ID Field

The `id` field in frontmatter should match the filename (without `.md`):

```yaml
---
id: task_research-can-bus-vs-spi-i2c
kind: Task
# ...
---
```

File: `research-can-bus-vs-spi-i2c.md`

## When Creating Tasks

1. **Think of a descriptive name** based on the task content
2. **Convert to kebab-case**: lowercase, hyphens for spaces
3. **Create file** with that name
4. **Set `id` field** to `task_<filename>`

## Examples by Task Type

**Research Tasks:**
- `research-can-bus-vs-spi-i2c.md`
- `research-tablet-options-touch-osc.md`
- `investigate-pcb-design-tools.md`

**Implementation Tasks:**
- `implement-can-bus-communication.md`
- `design-pcb-architecture.md`
- `refactor-firmware-ui-separation.md`

**Testing Tasks:**
- `test-decoupled-firmware-architecture.md`
- `test-touch-osc-interfaces.md`
- `validate-pcb-design.md`

**Administrative Tasks:**
- `purchase-tablets-touch-osc.md`
- `contact-chris-kuscinsky-can-bus.md`
- `pay-nyu-debt-retrieve-prototype.md`

