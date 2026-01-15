---
id: task_research-can-bus-vs-spi-i2c
kind: Task
status: pending
priority: high
urgency: short-term
project: Mutax
epic:
story:
parent:
blocked_by: []
blocks: []
due:
created: 2026-01-07
source: cap_2025-12-27T155249-0800.md
---

# Research CAN bus vs SPI/I2C for submodule communication

## Context

This task is part of the Mutax PCB architecture redesign. The system needs to connect multiple sequencer track modules to the main Teensy controller. The previous PCB design used USB for module communication, but this was identified as a flaw. We need to research and decide between CAN bus, SPI, and I2C for the submodule communication protocol.

This decision is critical because:
- It affects the overall system architecture
- It impacts PCB design and component selection
- It determines firmware communication patterns
- It blocks the PCB redesign work

## Notes

- Previous architecture used USB (identified as flawed)
- System needs to connect multiple modules (distributed encoder clusters per track)
- Main controller is Teensy 4.1
- Need to consider: distance, speed, reliability, complexity

## Acceptance Criteria

- [ ] Comparison document created covering CAN bus, SPI, and I2C
- [ ] Pros/cons listed for each protocol
- [ ] Recommendation made based on Mutax requirements
- [ ] Decision documented in project notes

