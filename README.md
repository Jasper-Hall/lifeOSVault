# lifeOSVault

LifeOS is a **Markdown-based cognitive scaffolding system** designed to support an ADHD user in building the life and future they desire, grounded in real constraints, energy limits, and material reality.

This vault is the **canonical, human-readable layer** of the LifeOS system.  
Everything here should remain understandable, inspectable, and usable even if all AI systems disappear.

LifeOS is not a productivity app, habit tracker, identity system, or life coach.  
It is infrastructure for **clarity, continuity, and agency**.

---

## Core Purpose

LifeOS exists to answer one question, consistently and honestly:

> **"Given my real constraints right now, what single action would best protect the future I'm trying to build — and how do I do it immediately?"**

The system achieves this by:
- holding context across time
- reducing ambiguity before applying urgency
- surfacing leverage points instead of task piles
- adapting to fluctuating energy, health, and finances
- quietly increasing agency over time

---

## Core Output Model

LifeOS has a **single focal pressure**, not a single concern.

### Primary Pressure (Singular)
At any given moment, the system may surface:

- **NOW** — the single most important action to take
- **WHY** — why it matters (goal / requirement context)
- **Root Blocker** — what is actually blocking progress
- **Action Handles** — concrete ways to act immediately

Only one primary action should ever demand attention.

### Contextual Scaffolding (Plural, Non-Urgent)
The system also *holds* (but does not demand action on):
- active commitments
- goals in progress
- blocked items and their causes
- upcoming time-sensitive concerns
- long-horizon pressures (health, finances, learning)

This separation is critical:
- **pressure must be singular**
- **awareness must be plural**

---

## Design Principles (Non-Negotiable)

1. Capture first, organize later  
2. Goals ≠ tasks  
3. Tasks exist to satisfy requirements  
4. Requirements block goals  
5. Constraints shape feasibility  
6. Reduce ambiguity before increasing pressure  
7. Critique constraints, not the user  
8. Never escalate via guilt or shame  
9. Support becoming, not optimization  
10. The system should fade when things are going well  
11. Categorize tasks by energy type, not track user energy state  

---

## What LifeOS Is Not

LifeOS is **not**:
- a chatbot
- a to-do list app
- a habit tracker
- a budgeting app
- a calendar replacement
- a motivational system
- an identity enforcement tool

LifeOS does not tell the user who to be.  
It does not moralize productivity or behavior.

---

## What LifeOS Is

LifeOS **is**:
- an externalized executive-function scaffold
- a memory and context holder
- a blocker-detection system
- a leverage-finding system
- a clarity engine
- a quiet support for long-term becoming

It helps the user:
- remember what matters
- act despite ambiguity
- adapt to real constraints
- compound effort into meaningful change

---

## Canonical Storage Philosophy

- **Markdown is the source of truth**
- **Git is the system of record**
- **Agents may propose, but code writes**
- **Human-authored intent is respected**
- **System-authored structure is allowed**

If a file cannot be understood without an AI, it does not belong here.

---

## Ownership Model

Files may include lightweight frontmatter to clarify ownership:

- `owner: human`
  - append-only or suggestion-only
  - never overwritten by agents

- `owner: system`
  - may be updated or regenerated
  - must remain readable and explainable

Ownership exists to preserve agency and trust.

---

## Vault Structure Overview

```
LifeOS/
├── 00_System/        # System state, snapshots, derived context
├── 10_Inbox/         # Raw captures (immutable)
├── 20_Commitments/   # Promises and obligations
├── 30_Projects/      # Multi-step efforts
├── 40_Goals/         # Outcomes and horizons
├── 50_Decisions/     # Recorded rationale
├── 60_Learning/      # Instrumental + ambient learning
├── 70_Narrative/     # Human-owned context (read-only to system)
├── 80_Inventory/     # Tools, assets, capabilities
└── 90_Archive/       # Completed or inactive material
```

Each section has its own README explaining its purpose and rules.

---

## Section Roles (High-Level)

### 00_System
System-owned state:
- financial summaries
- health / capacity context
- derived snapshots
Not hand-edited except intentionally.

### 10_Inbox
Raw capture only.
No organization.
No triage.
Immutable after creation.

### 20_Commitments
Things promised to others or to self.
Persist until resolved, renegotiated, or released.

### 30_Projects
Multi-step efforts with internal structure.
Projects are not task lists — they are contexts for leverage.

### 40_Goals
Outcomes, not actions.
Goals may be blocked by requirements.
Goals exist across time horizons.

### 50_Decisions
Important decisions and their rationale.
Used to prevent re-decision fatigue.

### 60_Learning
Two modes:
- **Instrumental learning** (to unblock goals)
- **Ambient learning** (low-pressure compounding)
No queues, no obligation.

### 70_Narrative
Human-owned context:
- intent
- values
- current season
- reflections
LifeOS may read this for context, but never prescribe identity.

### 80_Inventory
Material reality:
- tools
- assets
- access
- capabilities
- constraints
Used to assess feasibility and opportunity.

### 90_Archive
Nothing is deleted.
Completed or inactive material lives here.

---

## Learning Philosophy

Learning is valuable, but not all learning is urgent.

LifeOS supports:
- learning when it unblocks progress
- learning during low-energy or passive moments
- learning that compounds quietly over time

Learning is never used to delay action indefinitely.

---

## Relationship to AI / Agents

Agents are:
- helpers
- analysts
- planners
- summarizers

Agents are **not**:
- authorities
- memory stores
- identity holders
- decision-makers

The system should work imperfectly without AI.
AI improves clarity — it does not replace judgment.

### LifeOS Engine Skills

The LifeOS Engine provides agentic skills for automated processing:

- **process-inbox** - Process and triage inbox captures
- **categorize-content** - AI-powered content categorization with vault context
- **match-project** - Smart project matching with fuzzy search
- **create-commitment** - Create commitment files
- **create-decision** - Create decision files
- **update-goal** - Update goal files with progress notes
- **create-todo** - Handle todos (structure TBD)

Skills are located in `engine/.claude/skills/` and follow OpenSkills format.
Agents invoke skills via OpenCode/Claude Code CLI commands.

See `engine/AGENTS.md` for detailed skill documentation.

---

## Failure Modes to Avoid

- Turning LifeOS into a meta-project
- Over-analysis without action
- Excessive system complexity
- Decision outsourcing
- Guilt-driven pressure
- Identity enforcement

If any of these appear, the system should be simplified.

---

## Success Criteria

LifeOS is successful if:
- capture is reflexive
- ambiguity decreases
- follow-through improves
- momentum becomes more consistent
- low-capacity days do not cause collapse
- the system is used *less* when things are going well

Quiet success is the goal.

---

## Final Framing

LifeOS is a cognitive scaffolding system for becoming.

It helps the user:
- remember what matters,
- respect reality and constraints,
- reduce ambiguity at the moment of action,
- and quietly increase agency over time.

Not through pressure or optimization,
but through clarity, continuity, and care.
