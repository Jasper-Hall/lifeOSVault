---
id: project_mutax
status: active
horizon: mid
owner: human
created: 2018-01-01
last_reviewed: 2025-01-21
kind: Project
project: Mutax
parent: Rheome
priority: high
---

# Project: Mutax

## 1. What this project is (1–3 sentences)

Mutax is a hardware performance instrument designed specifically for fluid improvisation of live electronic music. It enables simultaneous control over core musical elements – rhythm, harmony, texture, and structure – through an interface rooted in expressive, tactile gestures, restoring immediacy, spontaneity and embodiment to electronic music performance. The system combines a retroactive MIDI looper, an algorithmic sequencer, and a gesture-controlled "mutation" engine that allows for generative control over all sequencer and looper tracks simultaneously, allowing users to quickly generate and record musical ideas and fluidly move them to new places with a single gesture.

---

## 2. Why it matters (intent context)

Existing electronic instruments often lack crucial features for live creation – they tend to be targeted towards playing back pre-composed patterns and typically lack the ability to make simultaneous changes across many tracks at once, making real-time composition cumbersome and limiting. More critically, electronic instruments often lack a meaningful connection between physical gesture and sound, unlike traditional acoustic instruments where expression and gesture are inherently linked. Mutax addresses both of these problems, allowing the user to simultaneously embody the roles of both a composer and a conductor, with their movements directly guiding the dynamics of their MIDI orchestra, for whom they are composing the score in real time.

If this never gets done, I'll continue to struggle with the limitations of existing hardware setups, unable to fully realize my vision of truly improvised live electronic music performance. The project represents 7 years of accumulated learning and frustration with existing solutions, and completing it would enable a new paradigm of live electronic music creation.

---

## 3. Current State
**Status:**  
- [] Active  
- [x] Blocked  
- [] Paused  

**Short summary:**  
Mutax exists as a physical prototype based on the Teensy 4.1 microcontroller hosted on the ProtoSupples Project System baseboard. The prototype contains an array of Adafruit modules (3 5x6 neokey matrices, 3 TCA8418 key matrix scanner ICs, 9 quad rotary encoder boards, and a Nintendo Wiichuck I2C breakout board) soldered to two perfboards. The firmware, written in C++ with AI coding assistance, contains a retroactive MIDI looper, an algorithmic sequencer, and a macro-level "mutation" engine with gesture control via the Wiichuck. However, the current prototype is unstable due to hardware issues (I2C address shifts, communication problems, wire-spaghetti nature with many potential points of failure) and is currently located at NYU Shanghai, inaccessible until a $450 debt is paid. The hardware prototype at NYU won't be used anymore - the main need is to test the firmware refactor where UI logic is decoupled from system logic (currently the firmware is one monolithic file with all UI code and business logic combined). Firmware refactoring work has been started but is not complete. A PCB was designed and ordered but got stuck in mail and was never delivered. The PCB design itself had flaws (wrong size cut holes for rear-mounted LEDs preventing pick-and-place assembly) and architectural issues (USB communication instead of CAN bus, incorrect distribution of components). The system architecture needs to be redesigned: sequencer/velocity-sensitive hall effect button grid should be centralized, with distributed individual encoder clusters for each sequencer track, using CAN bus for module communication rather than USB. An alternative path forward: purchase 2-3 tablets (similar cost to $450 debt) to use as prototyping surfaces for the physical UI using Touch OSC, allowing firmware testing without the hardware prototype.

---

## 4. Success Definition (Outcome, not tasks)

A stable, playable hardware instrument that enables completely improvised live electronic music sets from scratch, where the performer can fluidly transition between musical sections through expressive gestures rather than manual parameter adjustments. The instrument would allow for rapid idea generation through the retroactive looper and algorithmic sequencer, and seamless musical transitions through the archetype/gesture system. Success means being able to perform live sets that feel as immediate and embodied as playing a traditional acoustic instrument, with the complexity and power of electronic music production.

---

## 5. Root Blocker (single most important)

**Blocker type:** financial  
**Why this is the blocker:**  
The hardware prototype is currently at NYU Shanghai and cannot be retrieved until a $450 debt to NYU is paid off. However, the hardware prototype at NYU won't be used anymore - the main need is to test the firmware refactor where UI logic is decoupled from system logic. Without a way to test the firmware refactoring (either by retrieving the prototype or using an alternative like tablets with Touch OSC), development cannot continue. The firmware refactoring work has been started but is incomplete, and needs testing to ensure the system works when UI logic is decoupled from business logic. Additionally, the previously designed PCB was never delivered (stuck in mail) and had both manufacturing flaws (wrong size cut holes for rear-mounted LEDs) and fundamental architectural problems (USB instead of CAN bus, incorrect component distribution).

---

## 6. Immediate Leverage Point

**Primary Path:** Purchase 2-3 tablets (similar cost to $450 debt, ~$150-200 each) to use as prototyping surfaces for the physical UI using Touch OSC. This would allow testing of the firmware refactor without needing the hardware prototype at NYU. The firmware refactoring (decoupling UI logic from system logic) can be completed and validated using Touch OSC interfaces, ensuring the system works when UI and business logic are separated. This unlocks continued firmware development, testing of the mutation system, and sound design work without being blocked on hardware access.

**Alternative Path:** Once the $450 debt is paid and the prototype is retrieved, the immediate leverage point is redesigning the PCB architecture with the correct approach: using CAN bus for module communication (rather than USB), centralizing the sequencer/velocity-sensitive hall effect button grid, and distributing individual encoder clusters for each sequencer track. This corrected architecture would provide a stable development platform that allows firmware refinement, continued development of the mutation system, sound design work, and eventually industrial design for a compelling enclosure.

---

## 7. Action Handles (reduce ambiguity)

### Tasks
![[Project Management.base#Project Tasks]] 

### Epics
![[Project Management.base#Project Epics]]

### Stories
![[Project Management.base#Project Stories]] 

### Contextual Handles

- **Handle 1:** Financial
  - Type: financial
  - Target: Purchase 2-3 tablets (~$150-200 each, similar cost to NYU debt)
  - Notes: Use as prototyping surfaces for physical UI with Touch OSC. Allows testing firmware refactor (UI/business logic decoupling) without hardware prototype. Primary leverage point.

- **Handle 2:** Financial
  - Type: financial
  - Target: Pay $450 debt to NYU
  - Notes: Alternative path - required to retrieve hardware prototype from NYU Shanghai (though prototype won't be used, mainly needed for firmware testing)

- **Handle 3:** Document
  - Type: doc
  - Target: Intech Grid MIDI controller open-source schematics and PCB files
  - Notes: Leveraging these to develop custom PCB architecture. Need to redesign with CAN bus communication and proper component distribution (centralized button grid, distributed encoder clusters)

- **Handle 4:** Person
  - Type: person
  - Target: Chris Kuscinsky (Critter and Guitari)
  - Notes: Thesis mentor who suggested focusing on PCB development first. May need consultation on CAN bus architecture for multi-module systems

---

## 8. Dependencies & Related Work

- Goal(s): [[Hardware Performance Instrument Development]]
- Commitment(s): [[Thesis Project]]
- Related Projects: [[Rheome]]
- Decisions: [[PCB Development Approach]]

---

## 9. Open Questions / Uncertainties

- What is the optimal CAN bus architecture for connecting multiple sequencer track modules to the main Teensy controller?
- How many encoder clusters per track are needed, and what parameters should each cluster control?
- Should the centralized button grid handle all tracks or be track-specific?
- What is the optimal balance between firmware refinement, sound design, and industrial design priorities?
- How can the mutation system be expanded beyond the current harmonic and energetic categories?
- What is the best approach to user testing and iteration once hardware stability is achieved?

---

## 10. Learning / Capability Notes

- Missing / Partial Capability: PCB design, CAN bus architecture for embedded systems, advanced C++ for embedded systems, industrial design
- Suggested learning direction: 
  - PCB design: KiCad or Altium tutorials, studying Intech Grid schematics, learn proper component placement and cut hole sizing
  - CAN bus: Study CAN bus protocols for multi-module embedded systems, understand addressing and message routing
  - C++: Continue with AI-assisted development, deepen understanding of embedded systems
  - Industrial design: Parametric design class, study of existing electronic instrument enclosures
- Format preference (reading / video / audio): Video tutorials for PCB design and CAN bus, hands-on practice for all areas

---

## 11. Notes & Running Log (append-only)

- 2018 — Began journey trying to find/create live performance system for improvisation, started with Elektron Digitakt and Digitone
- 2018-2024 — Moved to Torso Electronics T-1 Algorithmic Sequencer, which opened eyes to possibilities of live electronic improvisation
- Fall 2024 — Critical Experiences class: daily improvisation exercises revealed that almost all desired changes were about shifts in energy or emotional quality of music. This insight led to Mutax concept ("Mut" = change, "ax" = state of)
- December 2024 — Final project for Critical Experiences: retroactive MIDI looper based on Teensy 4.1
- Spring 2025 — Thesis development: expanded UI with 2 additional Neokey matrices, 3 TCA8418 scan ICs, 8 more quad rotary encoder boards. Hardware integration proved most time-consuming part (weeks troubleshooting I2C address issues, key matrix scanning problems)
- Spring 2025 — User testing feedback: added loop start offset parameter, ability to change loop length after capture, support for different loop lengths per layer
- Spring 2025 — Implemented algorithmic sequencer with Euclidean algorithm + unique "distribution" parameter (weights pulses toward beginning/end of steps). Developed algorithm in JavaScript/Tone.js web app first, then ported to C++
- Spring 2025 — Implemented gesture-controlled archetype system: global TrackStates structure, global scale system, harmonic changes (scale degrees × chord types), energetic changes (increase, decrease, breakdown, 4 on the floor). Wiichuck Z-button triggers transition state where accelerometer affects sequencer pulses and joystick affects looper octave transposition
- Spring 2025 — Thesis presentation: 4 possible directions identified (PCB design, industrial design, firmware refinement, sound design). Mentor Chris Kuscinsky recommended PCB focus first due to hardware instability
- 2025-01-21 — Current plan: Develop modular PCB system based on Intech Grid schematics, create stable development platform before continuing other work
- 2025 — Designed first PCB: 4x4 mechanical hall effect key matrix (neopixel backlit), 12 push button encoders, 8 tactile switches, 1 mechanical key, OLED display, PSP joystick (too short), capacitive touch strip, ESP32S3 dev board as local MCU. Intended as dummy UI surface for one sequencer track, communicating with main Teensy 4.1 via USB. PCB got stuck in mail and was never delivered
- 2025 — Discovered PCB flaws: wrong size cut holes for rear-mounted LEDs (prevented pick-and-place assembly). Realized architecture is flawed: system should use CAN bus for module communication, not USB. Sequencer/button grid should be centralized, with distributed encoder clusters per track
- 2025 — Hardware prototype left at NYU Shanghai. Cannot retrieve until $450 debt to NYU is paid. Project currently blocked on financial and architectural redesign
- 2025 — Started firmware refactoring: decoupling UI logic from system/business logic. Currently one monolithic file with all UI code and business logic combined. Refactoring work in progress but incomplete. Need testing platform to validate decoupled architecture. Hardware prototype at NYU won't be used anymore - main need is for firmware testing
- 2025 — Alternative leverage point identified: Purchase 2-3 tablets (~$150-200 each) to use as prototyping surfaces with Touch OSC. Similar cost to NYU debt, allows firmware refactor testing without hardware prototype access

---



### Note from Inbox [2026-01-07]
I need to work on the mutax pcb and system architecture. research can bus vs spi/i2c for submodule communication
Source: cap_2025-12-27T155249-0800.md
## 12. Technical Details

### Hardware Architecture

**Current Prototype (at NYU Shanghai, inaccessible):**
- **Main Controller:** Teensy 4.1 microcontroller
- **Baseboard:** ProtoSupples Project System baseboard (prototyping PCB with MIDI IO, USB host, TFT touch display)
- **Input Modules:**
  - 3 × Adafruit 5x6 Neokey matrices (90 keys total)
  - 3 × TCA8418 key matrix scanner IC breakout boards
  - 9 × Quad rotary encoder boards
  - 1 × Nintendo Wiichuck I2C breakout board
- **Current Issues:** I2C address instability, communication problems requiring physical adjustment during bootup, wire-spaghetti nature with many failure points

**Attempted PCB Design (never delivered, flawed):**
- **Local MCU:** ESP32S3 dev board (header sockets)
- **Components:**
  - 4×4 mechanical hall effect key matrix (neopixel backlit)
  - 12 push button encoders
  - 8 tactile switches
  - 1 mechanical key
  - OLED display
  - PSP joystick (too short to reach enclosure surface)
  - Capacitive touch strip
- **Intended Function:** Dummy UI surface for one sequencer track (local scanning only, sends data packets to main MCU)
- **Communication:** USB to main Teensy 4.1 sequencer MCU
- **Flaws:**
  - Wrong size cut holes for rear-mounted LEDs (prevented pick-and-place machine assembly)
  - Architecture: Should use CAN bus for module communication, not USB
  - Component distribution: Sequencer/velocity-sensitive hall effect button grid should be centralized, not per-track
  - Should have distributed individual encoder clusters for each sequencer track, not all components on one per-track board

**Target Architecture (to be redesigned):**
- **Main Controller:** Teensy 4.1 (centralized)
- **Centralized Components:**
  - Sequencer/velocity-sensitive hall effect button grid
- **Distributed Components:**
  - Individual encoder clusters per sequencer track
- **Communication:** CAN bus for module-to-module communication

### Firmware Architecture
- **Language:** C++ (developed with AI assistance: Gemini 2.5 Pro, Claude 3.7, ChatGPT o1)
- **MIDI Clock:** Internal generation or external sync via uClock library
- **Current State:** Firmware is one monolithic file with all UI code and business logic combined. Refactoring work has been started to decouple UI logic from system logic, but is incomplete and needs testing.
- **Core Systems:**
  1. **Retroactive MIDI Looper:** Always-recording circular buffer on external PSRAM, time-stamped MIDI data. User selects loop length after playing, captures from buffer with optional loop-start offset. Supports modifiers: transposition, note probability, velocity offset, quantization
  2. **Algorithmic Sequencer:** Euclidean algorithm with distribution parameter (weights pulses toward beginning/end). Controlled via rotary encoders
  3. **Mutation Engine:** Global TrackStates structure contains all sequencer/looper parameters per track. Global scale system ensures harmonic coherence. Gesture control via Wiichuck:
     - Z-button hold: Transition state (accelerometer → sequencer pulses, joystick → looper octave transposition)
     - Z-button release: Applies cued harmonic and energetic changes simultaneously
- **Testing Strategy:** Touch OSC on tablets can serve as UI prototyping surface to test decoupled firmware architecture without hardware prototype access

### Key Innovations
- **MIDI-based looping** (vs. audio): Highly malleable starting point for applying changes
- **Distribution parameter:** Breaks out of Euclidean-only patterns by algorithmically shifting pulse weight
- **Simultaneous multi-track changes:** Single gesture applies harmonic and energetic shifts across all tracks
- **Retroactive capture:** Removes performance anxiety of red record button

---

## 13. Project References & Influences

### Key Artists & Systems
- **Beardyman's Beardytron:** Most advanced live production system, 5-iPad Touch OSC interface, macro transitions, retroactive looping
- **Tim Exile's Flow Machine:** Reaktor-based performance system with retroactive loopers, evolved into Endlesss iOS app/VST
- **Tim Exile's Scapeshift:** Generative groovebox with parametric sequencing, style-based randomization, state interpolation/morphing
- **Imogen Heap's Mi.Mu Gloves:** Configurable wearable MIDI interface with Glover software, controls Ableton Live project
- **Torso T-1 Algorithmic Sequencer:** First hardware instrument truly designed for improvised live electronic music performance
- **Onyx Ashanti:** 20-year development of 3D-printed wearable performance instrument, "beat-jazz" framework

### Research & Academic References
- **"Hands where we can see them!"** (Bin, Bryan-Kinns, McPherson): Research on audience perception of gesture size in electronic music performance
- **"Improvisation in Electronic Music—The Case of Vienna Electronica"** (Mazierska): Exploration of improvisation limits and instrument agency
- **"Play Along Mapping of Musical Controllers"** (Fiebrink, Cook, Trueman): Tool for interactively creating musical controller mappings using supervised machine learning

### Other Influences
- **STOOR:** Rotterdam-based venue/festival for live, collaborative, improvised electronic music
- **Author & Punisher:** Custom-made heavy, tactile controllers for industrial metal performance
- **Lambda Synthetic Polypulse:** Hardware instrument with algorithmic sequencing and capacitive touch pads for XY morphing

---

## 14. Credits & Acknowledgments

**Mentors & Contributors:**
- Craig Protzel
- Sarah Rothberg
- Sarah Hakani
- Nun
- Chris Kuscinsky (Critter and Guitari) - Thesis mentor
- Carrie Wang

**User Testers:**
- Ash Holloway
- Jahsiri Asabi Shakir
- Aaron Robins

**Development Tools:**
- Gemini 2.5 Pro
- Claude 3.7 Sonnet
- ChatGPT o1-Pro
- Cursor IDE

**Special Thanks:**
- Irwin Freundlich (grandfather) - Posthumously made this endeavor and master's program possible

---

