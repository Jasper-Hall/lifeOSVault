---
id: project_raybox
status: active
horizon: mid
owner: human
created: 2024-06-25
last_reviewed: 2025-01-21
kind: Project
project: Raybox
parent: null
priority: high
---

# Project: Raybox

## 1. What this project is (1–3 sentences)

Raybox is a **web-based generative visual tool** that turns music into **high-quality, audio-reactive video**, giving creators deep control without requiring TouchDesigner or After Effects experience. It sits **between professional procedural tools** and **templated "visualizer" apps**, combining the **speed and simplicity** of platforms like Renderforest or Spectrr with the **creative flexibility and real audio-driven modulation** you'd expect from TouchDesigner. Raybox provides a full **music-to-motion creation pipeline**, focused on visually distinctive content for online release rather than live VJ performance.

---

## 2. Why it matters (intent context)

Raybox is designed for anyone who needs to create **engaging, music-driven visuals for social media** and promotional assets, without hiring a motion designer. Core users include: **Music producers**, beat makers, and composers sharing previews on TikTok, Instagram, and YouTube; **Record labels**, **independent artists**, and **artist collectives** releasing new tracks and visuals; **Event promoters** and **venues** making short-form visuals for lineups, show announcements, and content campaigns; **Content creators** who want visuals that reflect their sound rather than a generic template.

If you've outgrown template-based visualizers but don't want to learn a node graph, Raybox is built for you. Raybox is **not a real-time VJ tool** — it's a **studio tool**. It delivers the **audio-reactive power of TouchDesigner** and the **speed of template-based visualizers**, without requiring node-based patching, complex rigging, or motion design experience. Where others offer one-click visuals that all look the same, Raybox gives you **your own look**, without the grind.

If this never gets done, creators will continue to struggle with the choice between expensive professional services, complex creative coding tools, or generic templates that don't reflect their unique sound and vision.

---

## 3. Current State
**Status:**  
- [x] Active  
- [ ] Blocked  
- [ ] Paused  

**Short summary:**  
Raybox exists as an advanced web-based platform with substantial infrastructure already built: stem separation via Spleeter, comprehensive audio analysis (BPM detection, transients, chroma, RMS), real-time Three.js visualization engine with multiple effects (metaballs, particle networks, bloom), unified timeline system with BPM-aware grid and snapping, asset collection system for slideshows, and a Remotion-based export pipeline foundation. The codebase has undergone significant cleanup (console logging removal, dead code elimination, audio hooks consolidation, rendering pipeline fixes), but critical MVP features remain incomplete: persistent editing/auto-save, audio caching persistence, simplified parameter mapping UI, professional timeline with resizable clips, functional render pipeline, and credit system. The platform is currently in active development toward MVP, with the timeline system and BPM detection recently completed, but the export pipeline and several core user experience features still need implementation.

---

## 4. Success Definition (Outcome, not tasks)

A stable, production-ready SaaS platform where a user can upload an audio file, see automatic stem separation and analysis, create a compelling visualization by mapping audio features to visual effects using an intuitive interface, edit their composition on a professional timeline with BPM-aware snapping, and export a high-quality video file—all within minutes, without technical knowledge. Success means users can create professional music visualizations that rival manually-produced content, with the platform handling all the complex audio analysis, feature extraction, and rendering automatically. The platform should feel as immediate and accessible as uploading a photo to Instagram, but produce results that look professionally produced.

---

## 5. Root Blocker (single most important)

**Blocker type:** technical / architectural  
**Why this is the blocker:**  
The codebase has substantial infrastructure but lacks the cohesive user experience flow required for MVP. The primary blocker is the incomplete integration between the sophisticated backend systems (audio analysis, stem separation, database) and the frontend user experience (timeline editing, parameter mapping, video export). Specifically: (1) The render pipeline exists in foundation but is not functional end-to-end—users cannot actually export videos yet, (2) Persistent editing and auto-save are missing, meaning users lose work on refresh, (3) The parameter mapping interface is complex and not simplified for non-technical users, (4) Audio analysis results are not cached persistently, causing re-analysis on every page load. These gaps prevent the platform from delivering its core value proposition: a seamless, accessible tool for creating professional music visualizations. The technical debt from rapid AI-assisted development (monolithic components, mixed state management patterns) also creates maintenance challenges that slow feature development.

---

## 6. Immediate Leverage Point

**Primary Path:** Complete the MVP consolidation roadmap (Phase 1-3 from the rolling todo list) by focusing on the critical user experience gaps: (1) Implement persistent editing and auto-save to prevent work loss, (2) Add audio caching persistence to eliminate re-analysis overhead, (3) Simplify the parameter mapping interface to match MIDI-like control patterns, (4) Complete the Remotion render pipeline to enable actual video export, (5) Implement the credit system for production readiness. These five features transform the platform from a sophisticated technical demo into a usable product. The infrastructure is already built—what's needed is the polish and integration work to make it accessible to end users.

**Alternative Path:** If technical debt becomes too burdensome, pause feature development and conduct a focused architectural refactor: break down the monolithic `creative-visualizer/page.tsx` (1,756 lines) into smaller components, standardize state management patterns, and complete the multi-layer compositor architecture. This would improve maintainability and unlock faster feature development, but delays MVP launch.

---

## 7. Action Handles (reduce ambiguity)

### Tasks
![[Project Management.base#Project Tasks]] 

### Epics
![[Project Management.base#Project Epics]]

### Stories
![[Project Management.base#Project Stories]] 

### Contextual Handles

- **Handle 1:** Technical - Complete persistent editing and auto-save system
- **Handle 2:** Technical - Implement audio caching persistence  
- **Handle 3:** Technical - Simplify parameter mapping interface
- **Handle 4:** Technical - Complete Remotion render pipeline
- **Handle 5:** Technical - Implement credit system
- **Handle 6:** Technical - Build professional timeline with resizable clips
- **Handle 7:** Technical - Create compelling landing page with email capture
- **Handle 8:** Technical - Integrate advanced drum stem separation via music.ai

*Note: Detailed technical handles have been moved to epics, stories, and tasks. See embedded views above.*

---

## 8. Dependencies & Related Work

- Goal(s): [[Music Visualization Platform MVP]]
- Commitment(s): [[SaaS Product Launch]]
- Related Projects: None
- Decisions: [[Timeline Architecture Decision]], [[Render Pipeline Architecture Decision]], [[State Management Pattern Decision]]

---

## 9. Open Questions / Uncertainties

- What is the optimal balance between automated analysis and user control in the parameter mapping interface?
- Should the platform support real-time collaboration features, or focus on single-user workflows for MVP?
- What is the best pricing model for credits (per-minute of video, per-stem-separation, subscription tiers)?
- How should the platform handle very long audio files (10+ minutes) for analysis and rendering?
- What is the optimal number of visual effects to offer in the MVP (currently targeting 5-10)?
- Should MIDI functionality be fully integrated or kept as an optional advanced feature?
- What level of customization should users have over visual effects (presets only vs. full parameter control)?
- How should the platform handle edge cases in audio analysis (very quiet tracks, non-musical audio, corrupted files)?
- What is the best approach to user onboarding and tutorials for non-technical users?
- Should the platform support batch processing of multiple audio files, or focus on single-file workflows for MVP?

---

## 10. Learning / Capability Notes

- Missing / Partial Capability: Remotion advanced rendering patterns, AWS Lambda integration for serverless rendering, credit system design and Stripe integration, user onboarding UX design, performance optimization for large audio files
- Suggested learning direction: 
  - Remotion: Study Remotion documentation for programmatic rendering, frame-by-frame state management, deterministic rendering patterns
  - AWS Lambda: Learn serverless architecture patterns, Lambda function optimization, queue-based job processing
  - Stripe: Study credit system design patterns, subscription management, webhook handling
  - UX Design: Research onboarding best practices for creative tools, progressive disclosure patterns, tutorial systems
  - Performance: Learn audio processing optimization, Web Worker patterns, memory management for large files
- Format preference (reading / video / audio): Video tutorials for Remotion and AWS Lambda, hands-on practice for all areas, documentation reading for API integrations

---

## 11. Notes & Running Log (append-only)

- 2024-06-25 — Project initialized as "Phonoglyph" with initial PRD and architecture documentation
- 2024-06-26 — Added stem separation and audio analysis to PRD
- Fall 2024 — Rapid AI-assisted development phase: built monorepo structure, Next.js frontend, Express.js backend, Supabase integration, tRPC API, Three.js visualization engine
- 2024-10-22 — Modular effects system implemented: EffectRegistry architecture replaces hardcoded if/else conditionals, enables scalable effect addition
- 2024-10-23 — Console logging cleanup completed: replaced 500+ console statements with debugLog/logger system, eliminated production console spam
- 2024-10-23 — Audio hooks consolidation: merged three overlapping hooks (use-audio-analysis, use-enhanced-audio-analysis, use-cached-stem-analysis) into single unified hook, 47% code reduction
- 2024-10-28 — Rendering pipeline refactor completed: fixed critical transparency issues, implemented alpha-preserving post-processing (Bloom, FXAA), added controllable background layer, fixed multi-layer compositing
- 2024-12 — Tech debt audit completed: identified AI-generated bloat, structural complexity, dead code. Overall health score: 6.2/10. Quick wins completed (console cleanup, dead code removal, audio hooks consolidation)
- 2025-01-21 — Timeline system overhaul completed: unified timeline layout with aligned track headers and lanes, implemented BPM-aware grid and snapping, added zoom functionality (0.1x to 10x), integrated dnd-kit for interactive layer clips
- 2025-01-21 — BPM detection implemented: integrated web-audio-beat-detector, added BPM to audio analysis data structure, displayed BPM in creative-visualizer top bar, grid lines align with waveforms
- 2025-01-21 — Asset collection system completed: database migration for asset_collections and asset_collection_items tables, tRPC endpoints for collection management, image slideshow feature foundation
- 2025-01-21 — Current focus: MVP consolidation roadmap. Remaining critical features: persistent editing/auto-save, audio caching persistence, simplified parameter mapping, functional render pipeline, credit system, professional timeline completion, landing page
- 2025-01-21 — Project renamed from "Phonoglyph" to "Raybox" for clearer branding and market positioning

---

## 12. Technical Details

### Architecture

**Monorepo Structure:**
- **Frontend:** `apps/web/` - Next.js 14.1.0 with TypeScript 5.3.3, Tailwind CSS, shadcn/ui components
- **Backend:** `apps/api/` - Express.js 4.18.2 with TypeScript 5.3.3, tRPC 10.45.2, PostgreSQL 16.1 (Supabase)
- **Shared:** `packages/` - Shared TypeScript types and configurations

**Tech Stack:**
- **Frontend:** Next.js, React, TypeScript, Three.js, Tailwind CSS, shadcn/ui, Zustand (minimal), dnd-kit, Remotion
- **Backend:** Express.js, tRPC, PostgreSQL (Supabase), AWS S3, Cloudflare R2, RunPod (for Spleeter stem separation)
- **Audio Processing:** Web Audio API, Meyda (audio analysis), web-audio-beat-detector (BPM), Spleeter (stem separation)
- **Visualization:** Three.js, EffectComposer, UnrealBloomPass, FXAA, custom shaders
- **State Management:** React Context + Domain Hooks (primary), Zustand (timeline store), React Query (server data)

### Core Systems

**1. Audio Analysis Pipeline:**
- **Worker:** `apps/web/public/workers/audio-analysis-worker.js` - Web Worker for non-blocking audio analysis
- **Features Extracted:** RMS, loudness, spectralCentroid, FFT, transients, chroma (pitch), BPM
- **Caching:** Analysis results stored in Supabase database (currently not persistent across sessions)
- **Integration:** Unified `useAudioAnalysis` hook provides single API for all audio analysis needs

**2. Stem Separation:**
- **Backend Service:** Spleeter-based separation via RunPod infrastructure
- **Stems:** Drums, bass, vocals, other
- **Storage:** Stem files stored in Cloudflare R2, metadata in Supabase
- **Future:** Integration with music.ai API for per-drum stem separation (kick, snare, hats, percussion)

**3. Visualization Engine:**
- **Core:** `VisualizerManager.ts` (877 lines) - Manages Three.js scene, effects, compositing
- **Compositor:** `MultiLayerCompositor.ts` - Multi-layer rendering with alpha-preserving post-processing
- **Effects System:** Registry-based architecture (`EffectRegistry.ts`) - Currently supports: metaballs, particleNetwork, bloom
- **Effects:** Each effect manages its own THREE.Scene, implements VisualEffect interface
- **Post-Processing:** Bloom pass (alpha-preserving), FXAA (alpha-preserving), texture pass

**4. Timeline System:**
- **Component:** `UnifiedTimeline.tsx` - Professional timeline with BPM-aware grid
- **Store:** `timelineStore.ts` (Zustand) - Centralized timeline state (layers, currentTime, zoom, selectedLayerId)
- **Features:** Zoom (0.1x to 10x), BPM-aware grid lines, snap-to-grid, draggable/resizable layer clips via dnd-kit
- **Integration:** Pulls state directly from store, no props drilling

**5. Asset Management:**
- **Collections:** Database tables for `asset_collections` and `asset_collection_items`
- **Types:** Image slideshow, generic collections
- **Storage:** Files stored in Cloudflare R2, references in Supabase
- **UI:** Collection creation and management via tRPC endpoints

**6. Render Pipeline (In Progress):**
- **Foundation:** Remotion integration started, not yet functional
- **Target:** Headless frame renderer that can deterministically render visual state for any time point
- **Architecture:** Remotion composition calls `renderFrame` function for each frame
- **Backend:** `project.createRenderJob` tRPC endpoint (to be implemented)
- **Execution:** In-process rendering for MVP (not scalable, will migrate to background worker post-MVP)

### Key Innovations

- **Automated Feature Extraction:** Automatic BPM detection, transient detection, pitch analysis, volume analysis from any audio file
- **Registry-Based Effects System:** Scalable architecture for adding new visual effects without touching core code
- **Multi-Layer Compositing:** Alpha-preserving post-processing pipeline with proper transparency handling
- **BPM-Aware Timeline:** Musical grid that adapts to song tempo, enabling rhythmically-aligned editing
- **Unified Audio Analysis:** Single hook API that consolidates all audio analysis features (RMS, transients, chroma, BPM)

### Current Technical Debt

- **Monolithic Components:** `creative-visualizer/page.tsx` (1,756 lines) needs refactoring into smaller components
- **State Management:** Multiple overlapping patterns (React Context, Zustand, local state) need standardization
- **Render Pipeline:** Foundation exists but not functional end-to-end
- **Audio Caching:** Analysis results not persisted across browser sessions
- **Parameter Mapping:** Complex UI needs simplification for non-technical users

---

## 13. Project References & Influences

### Key Products & Tools
- **TouchDesigner:** Professional node-based visual programming platform (complexity we're avoiding)
- **p5.js:** Creative coding library (technical barrier we're removing)
- **After Effects:** Industry standard for motion graphics (manual keyframing we're automating)
- **Remotion:** React-based video creation framework (our export pipeline foundation)
- **Spleeter:** Audio source separation (our current stem separation solution)
- **music.ai:** Advanced stem separation API (future integration target)

### Research & Academic References
- **Web Audio API:** Browser-based audio processing standard
- **Three.js:** 3D graphics library for web
- **tRPC:** End-to-end typesafe APIs
- **Supabase:** Open-source Firebase alternative

### Design Influences
- **shadcn/ui:** Modern React component library (our UI foundation)
- **Glassmorphism:** Modern UI design trend (our design system aesthetic)
- **Professional DAWs:** Timeline interfaces from Ableton Live, Logic Pro (our timeline inspiration)

---

## 14. Credits & Acknowledgments

**Development Tools:**
- Cursor IDE
- AI Coding Assistants (Claude, ChatGPT, Gemini)
- TypeScript
- Next.js
- Three.js
- Remotion

**Infrastructure & Services:**
- Supabase (database, auth, storage)
- Cloudflare R2 (file storage)
- AWS S3 (backup storage)
- RunPod (Spleeter stem separation)
- Vercel (frontend deployment)

**Open Source Libraries:**
- Three.js
- Remotion
- tRPC
- dnd-kit
- web-audio-beat-detector
- Meyda
- shadcn/ui

**Special Thanks:**
- The open-source community for the incredible tools that make this project possible
- Early testers and feedback providers (to be added as project progresses)

---

