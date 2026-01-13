---
id: task_complete-remotion-pipeline
kind: Task
status: pending
priority: high
urgency: immediate
project: Raybox
epic: epic_video-export
story: story_beat-synced-export
parent: story_beat-synced-export
blocked_by: []
blocks: [story_multi-aspect-pipeline]
due: 
created: 2026-01-07
source: 
---

# Complete Remotion render pipeline

## Context

Render pipeline foundation exists but is not functional end-to-end. Users cannot actually export videos yet. Critical for MVP.

## Notes

- Build headless frame renderer
- Create Remotion composition
- Implement `project.createRenderJob` tRPC endpoint
- Execute render in-process for MVP
- File targets: `apps/web/src/lib/remotion/`, `apps/api/src/routers/project.ts`

## Acceptance Criteria

- [ ] Headless frame renderer functional
- [ ] Remotion composition created
- [ ] Render job endpoint implemented
- [ ] Video export works end-to-end
- [ ] High-quality output





