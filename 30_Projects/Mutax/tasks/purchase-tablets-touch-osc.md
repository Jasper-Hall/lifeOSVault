---
id: task_purchase-tablets-touch-osc
kind: Task
status: pending
priority: high
urgency: immediate
project: Mutax
epic:
story:
parent:
blocked_by:
  - constraint_financial
blocks:
  - task_complete-firmware-refactoring
  - task_test-decoupled-firmware-architecture
due:
created: 2025-01-21
source:
---

# Purchase 2-3 tablets for Touch OSC prototyping

## Context

The hardware prototype is currently at NYU Shanghai and cannot be retrieved until a $450 debt is paid. However, the hardware prototype won't be used anymore - the main need is to test the firmware refactor where UI logic is decoupled from system logic.

Purchasing 2-3 tablets (~$150-200 each) provides an alternative path:
- Similar cost to NYU debt
- Allows firmware refactor testing without hardware prototype access
- Enables Touch OSC interfaces for UI prototyping
- Unblocks firmware development work

This is the primary leverage point for unblocking the project.

## Notes

- Cost: ~$150-200 per tablet (2-3 tablets needed)
- Use case: Touch OSC interfaces for physical UI prototyping
- Enables: Firmware refactor testing (UI/business logic decoupling)
- Alternative to: Paying $450 NYU debt to retrieve hardware prototype

## Acceptance Criteria

- [ ] Research tablet options (compatibility with Touch OSC, price, availability)
- [ ] Purchase 2-3 tablets
- [ ] Set up Touch OSC interfaces for Mutax UI
- [ ] Verify tablets can serve as prototyping surface for firmware testing

