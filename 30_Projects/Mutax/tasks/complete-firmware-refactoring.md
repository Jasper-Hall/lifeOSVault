---
id: task_complete-firmware-refactoring
kind: Task
status: in_progress
priority: medium
urgency: short-term
project: Mutax
epic:
story:
parent:
blocked_by:
  - task_purchase-tablets-touch-osc
blocks:
  - task_test-decoupled-firmware-architecture
due:
created: 2025-01-21
source:
---

# Complete firmware refactoring (decouple UI from business logic)

## Context

The current firmware is one monolithic file with all UI code and business logic combined. This makes the codebase difficult to maintain and test. The refactoring work has been started but is incomplete.

The goal is to decouple UI logic from system/business logic so that:
- UI can be tested independently (e.g., with Touch OSC)
- Business logic can be tested without hardware
- Code is more maintainable and modular
- System works when UI and business logic are separated

## Notes

- Refactoring work in progress but incomplete
- Currently one monolithic file
- Need testing platform to validate decoupled architecture
- Blocked by: Need tablets (task_002) for testing

## Acceptance Criteria

- [ ] UI logic separated from business logic
- [ ] Modular architecture implemented
- [ ] Code compiles and runs
- [ ] Architecture validated with Touch OSC testing

