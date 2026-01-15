---
id: project_tombogo-x-rheome
status: active
horizon: mid
owner: human
created: 2026-01-07
last_reviewed: 2026-01-07
kind: Project
project: tombogo-x-rheome
priority: high
---

# Project: Tombogo x Rheome Collaboration

## 1. What this project is (1–3 sentences)

Collaboration between Tombogo and Rheome to develop a wearable hardware gadget—a functional creative tool with minimal UI, Tamagotchi-like interactive/playful/alive feeling. The device will be a wearable accessory (bag charm, worn around neck, or clipped to belt) that's intentionally lofi and minimal, more of a "sketchbook" than a "studio" tool. Target price range $150-250 with 6-7 month development timeline targeting late November 2025 release.

## 2. Why it matters (intent context)

This collaboration solves a critical distribution problem for Rheome. Tombogo has an established audience, which means:
- No need to market, fulfill orders, or fund the launch independently
- Leveraging Tombogo's existing audience and infrastructure
- Receiving 50% of profits after Tombogo recoups expenses

**Financial Impact:**
Based on the success of Pocketcam (thousands sold at roughly $175, generating hundreds of thousands in revenue for Tombogo), even a 30-50k revenue split would majorly extend runway and help bring Rheome to life. This financial boost is critical given the current income gap and need for additional revenue sources.

**Personal Context:**
This project emerged after losing our close high school friend Tariq. Tommy and I had drifted apart since high school, and this collaboration is an effort to turn that tragedy into something positive—reconnecting through creative collaboration and building something meaningful together.

**Strategic Benefits:**
- Establishing Rheome's presence in the music technology community
- Building audience and social media presence ahead of the launch
- Creating a tangible product that demonstrates Rheome's capabilities
- Generating momentum for the broader Rheome brand and ecosystem
- Financial runway extension without the burden of full distribution responsibilities

The November launch is expected to drive significant audience and attention to Rheome, making the social presence and internet infrastructure critical preparation work.

## 3. Current State

**Status:**  
- [x] Active  
- [ ] Blocked  
- [ ] Paused  

**Short summary:**  
Project is in early stages. Need to begin work on prototype development with target completion by July 2025, preparing for November 2025 launch.

## 4. Success Definition (Outcome, not tasks)

A finalized, tested prototype ready for production by July 2025, with all launch preparation complete for late November 2025 release. The product meets the design criteria: form-first, functional creative tool with minimal UI, Tamagotchi-like interactive/playful/alive feeling, wearable accessory aesthetic, intentionally lofi and minimal (sketchbook not studio), real functionality (not gimmicky), priced at $150-250 with target $50-60 cost for 75% margin at $250 price point. The collaboration successfully showcases Rheome's capabilities and generates significant audience growth and industry attention.

## 5. Root Blocker (single most important)

**Blocker type:** access  
**Why this is the blocker:**  
Waiting on Tommy (Tombogo) to add ideas to the Notion page and schedule another call to confirm the final product concept. Cannot begin prototyping until the final idea is confirmed and agreed upon by both parties.

## 6. Immediate Leverage Point

**Primary Path:** [To be determined - need to clarify project scope and requirements]  

**Alternative Path:** [Alternative approach if primary path isn't available]

## 7. Action Handles (reduce ambiguity)

### Tasks

![[Project Management.base#Project Tasks]]

### Epics

![[Project Management.base#Project Epics]]

### Stories

![[Project Management.base#Project Stories]]

### Contextual Handles

- **Handle 1:** [Type] - [Description]
- **Handle 2:** [Type] - [Description]

## 8. Dependencies & Related Work

- Goal(s): [[Mid-Term_Goals#Tomobo Collab Prototype Complete]], [[Mid-Term_Goals#Rheome Social Presence & Audience Building]]
- Commitment(s): 
- Related Projects: [[Rheome]]
- Decisions: 

## 9. Open Questions / Uncertainties

### Product Concept
- Which concept will be developed? (Audio diary, mini sampler/groovebox, clock/watch, or other?)
- How will Tommy's ideas (Pocket Cam successor, LiDAR, MIDI bag) integrate with Jasper's concepts?
- What specific functionality will differentiate this from existing products?

### Technical Decisions
- Which development platform: Electrosmith Daisy, ESP32, or RP2040/RP2350?
- What are the audio processing requirements?
- What sensors/inputs are needed?
- Battery life and power management requirements?

### Design & Production
- Final form factor and industrial design
- Manufacturing approach and cost structure
- Timeline for prototype milestones (target July completion, November launch)

## 10. Learning / Capability Notes

- Missing / Partial Capability: [to be identified]
- Suggested learning direction: [to be determined]
- Format preference: [reading / video / audio]

## 11. Notes & Running Log (append-only)

**2026-01-07:** Project initiated. Product criteria and concept ideas documented. Multiple concept directions under consideration (audio diary, mini sampler/groovebox, clock/watch). Development platform comparison completed (Daisy, ESP32, RP2040/RP2350). Target: prototype complete by July 2025, launch late November 2025.

## 12. Technical Details

### Product Criteria

- **Form first** - Aesthetic and physical design is primary
- **Functional creative tool** - Real utility, not novelty
- **Minimal UI** - Simple, intuitive interface
- **Tamagotchi vibes** - Interactive, playful, alive feeling
- **Wearable accessory** - Bag charm, neck-worn, or belt-clipped (not fabric/garment incorporated)
- **Sketchbook aesthetic** - Intentionally lofi and minimal, more "sketchbook" than "studio"
- **Real functionality** - Not gimmicky or pure novelty
- **Price range:** $150-250 (target $50-60 cost for 75% margin @ $250 price)
- **Timeline:** 6-7 months targeting late November 2025 release

### Concept Ideas

#### Jasper's Concepts
- **"Audio diary"** - Turn your day into loops
  - Device with on-board mic, records snippets throughout the day (manually or automatically)
  - On-board generative algorithms process recordings into loops/samples
  - Examples: resonator algorithm turns ambience into chord progressions, chopper algorithm turns textures into rhythms
  - Reference: [XLN Audio Life](https://www.xlnaudio.com/products/life)
- **Pocket Operator-esque mini sampler/groovebox** with minimal UI and wearable accessory aesthetic
  - Reference: [Zeptocore](https://zeptocore.com/)
- **Clock/Gogo-gadget watch/timepiece**

#### Tommy's Concepts
- Successor to Pocket Cam, LiDAR?
- MIDI bag

### Inspiration & Reference Products

- **Terra** - [myterra.ai](https://www.myterra.ai/)
- **Teenage Engineering TP-7** - [teenage.engineering/store/tp-7](https://teenage.engineering/store/tp-7)
- **Meng Qi Wingie 2** - [mengqimusic.com/shop-base/p/wingie2](https://www.mengqimusic.com/shop-base/p/wingie2)
- **Noware Puff** - [noware.nyc](https://www.noware.nyc/)

### Development Platform Comparison

| Platform | Pros | Cons | Reference Projects |
|----------|------|------|-------------------|
| **Electrosmith Daisy** | Audio-centric, built-in DAC/ADC, codec, amp, RAM. DIY-friendly audio development ecosystem (pure data, gen~ support). Made by Electrosmith in LA, team is accessible and supportive | Expensive ($21/board, DFM version requires application), no built-in WiFi/bluetooth, larger form factor | [Daisy in the Wild - Hichord](https://electro-smith.com/blogs/seeds-n-circuits/daisy-in-the-wild-hichord), [Componental](https://www.componental.co/) |
| **ESP32** | Super cheap, ubiquitous. WiFi and Bluetooth built-in. Popular with lots of open source examples. Dual core CPU | No built-in audio circuitry (adds cost and dev complexity). Custom boards require navigating RF/wireless difficulties. Not as powerful as Daisy | [Wildwoods Soundworks](https://wildwoodssoundworks.com/), [YouTube example](https://www.youtube.com/watch?v=4N-xwM3L7KI) |
| **RP2040/RP2350** | Dirt cheap, fast. Many DIY synth/audio projects use these. Developed by Raspberry Pi foundation with strong community and dev support | No WiFi/bluetooth, no built-in audio circuitry. Analog inputs have some issues (may need workarounds for analog sensors) | [Zeptocore](https://zeptocore.com/), [Wee Noise Makers PGB-1](https://www.crowdsupply.com/wee-noise-makers/wee-noise-makers-pgb-1) |

### Platform Decision Notes

- **Daisy** offers best audio capabilities but higher cost and larger size
- **ESP32** provides connectivity but requires additional audio hardware
- **RP2040/RP2350** is cost-effective with good community support but lacks connectivity and has analog input limitations

Decision pending based on final product concept and requirements.

