# Open Design and Technology  
## Final Project README

> **Project Weight:** 70%  
> **Team Size:** 2 students  
> **Project Duration:** 4 weeks  
> **Class Time Available:** 6 hours per class  
> **Total Time Available:** 48 effort-hours per team  
> **Project Type:** Playful, interactive, technology-based experience

---

# Before you begin

## Fork and rename this repository
After forking this repository, rename it using the format:

`ODT-2026-TeamName`

### Example
`ODT-2026-PixelWizards`

Do not keep the default repository name.

---

# How to use this README

This file is your team’s **working project document**.

You must keep updating it throughout the 4-week build period.  
By the final review, this README should clearly show:
- your idea,
- your planning,
- your design decisions,
- your technical process,
- your build progress,
- your testing,
- your failures and changes,
- your final outcome.

## Rules
- Fill every section.
- Do not delete headings.
- If something does not apply, write `Not applicable` and explain why.
- Add images, screenshots, sketches, links, and videos wherever useful.
- Update task status and weekly logs regularly.
- Use this file as evidence of process, not only as a final report.

---

# 1. Team Identity

## 1.1 Studio / Group Name
`Magic Piano`

## 1.2 Team Members

| Name | Primary Role | Secondary Role | Strengths Brought to the Project |
|---|---|---|---|
| Risha Salunkhe | Physical set up and circuit connections | Song choice and gameplay | Physical fabrication, MDF build, foil pad assembly, wiring, circuit connections |
| Swaranjali Garima | Coding and interface design | Presentation layout and instructions | MicroPython on ESP32, Python game logic on laptop, screen visuals, sound triggering|

## 1.3 Project Title
 Dard-E-Disco
 
 ## 1.4 One-Line Pitch
A physical touch-pad table where players follow a song sequence shown on a screen by tapping the correct foil pad — like Magic Tiles, but real and tangible.`

## 1.5 Expanded Project Idea
In 1–2 paragraphs, explain:
- what your project is,
- what kind of playful experience it creates,
- what makes it fun, curious, engaging, strange, satisfying, competitive, or delightful,
- what technologies are involved.

**Response:**  
Magic Piano is a physical, multiplayer music game built on a 4×3 ft MDF table. Eight touch-sensitive pads, made from aluminium foil wrapped around foamboard, sitting in cutout windows in the MDF, represent the eight notes of a musical octave (C D E F G A B C5). A screen (projected via a projector positioned beside or behind the table) displays a piano keyboard. The keys on screen light up one at a time in a song sequence. Each key on the screen is spatially aligned with its corresponding physical pad on the table, the player simply looks at the glowing key and taps the pad directly in front of it.
When the correct pad is touched, the ESP32 detects the contact and sends a signal to the laptop. A Python script on the laptop receives this, confirms the correct touch, plays the corresponding piano note through the laptop speakers, and advances the sequence on screen. A wrong touch plays an error sound and resets the sequence to the beginning. Up to four players stand at one side of the table and share the tapping. The experience requires no instructions, the glowing key on screen tells you exactly what to do, and the position of the pad in front of it tells you where to tap.

---

# 2. Philosophy Fit

## 2.1 Experience, Not Social Problem
This module does **not** require your project to solve a large social problem.

You are allowed to build:
- toys,
- games,
- interactive objects,
- playful machines,
- kinetic artifacts,
- humorous devices,
- strange but delightful experiences,
- things that are entertaining to use or watch.

## 2.2 What kind of experience are you creating?
Answer the following:
- What is the experience?
- What do you want the player or participant to feel?
- Why would someone want to try it again?

**Response:**  
The experience is a cooperative and competitive music-following game played on a physical table. Players feel the excitement of hitting the right note at the right moment, and the tension of not breaking the chain. The screen gives a clear cue, the foil pad gives a real tactile surface to press, and the sound gives immediate confirmation. Players want to try again because the reset is instant, the challenge is intuitive, and completing a full song together is genuinely satisfying. The physicality of pressing a real pad, rather than a touchscreen, makes the experience feel more deliberate and rewarding.

## 2.3 Design Persona
Complete the sentence below:

> We are designing this project as if we are a small creative studio making a **[toy / game / playable object / interactive experience]** for **[children / teens / adults / classmates / exhibition visitors / mixed audience]**.

**Response:**  
We are designing this project as if we are a small creative studio making a playable interactive installation for a mixed audience of all ages at a college exhibition.

---

# 3. Inspiration

## 3.1 References
List what inspired the project.

| Source Type | Title / Link | What Inspired You |
|---|---|---|
| App | https://play.google.com/store/apps/details?id=com.youmusic.magictiles&hl=en_IN | The core mechanic, tapping the correct tile in a sequence to play a song. We borrowed the visual cue system (one tile lights up at a time) and the immediate correct/wrong feedback loop. |
| Game| The Floor is Lava |The physical urgency of having to react quickly to a spatial cue. Inspired the idea of making a screen-based game feel physical and embodied. |
| Movie | Dhurandhar- The Revenge [Part 2] | Thematic inspiration and reference- we used the song from this movie |

## 3.2 Original Twist
What makes your project original?

**Response:**  
Magic Piano takes a mobile game mechanic and makes it fully physical. Instead of tapping a screen, players touch real pads embedded in a real table, with a real projector overhead. The social dimension, four players at one table, sharing a song, is something the mobile version cannot replicate. The handmade quality of the build (foil pads, MDF cutouts) gives it a raw, workshop feel that contrasts with the clean projected interface above it.

---

# 4. Project Intent

## 4.1 Core Interaction Loop
Describe the main loop of interaction.

Examples:
- press → launch → score → reset
- connect → control → observe → repeat
- turn → trigger → react → repeat
- move object → sensor detects → sound/light response → player reacts

**Response:**  
key glows on screen → player identifies corresponding pad by position → player taps pad → ESP32 detects touch → laptop plays note + advances sequence → wrong tap → error sound + reset → repeat until song completes

## 4.2 Intended Player / Audience

| Question | Response |
|---|---|
| Who is this for? | Exhibition visitors, college students, general public |
| Age range | All ages — 8 and above |
| Solo or multiplayer | Up to 4 players simultaneously, same side of table |
| Expected duration of one round | 2–3 minutes |
| What should the player feel? | Excitement, musical satisfaction, mild competitive tension, delight at making music together |
| Is explanation required before use? | No, the glowing screen key aligned with the physical pad is self-explanatory. We will have a short brief instructions slide |

## 4.3 Player Journey
Describe exactly how a player will use the project.

1. **Approach:**  Player sees a table with 8 plain foil pads and a screen beside it showing a piano keyboard. The display scene shows "Dard-e-Disco".
2. **Start:** The experience begins when the player clicks a Start button on screen (or when the slide switches into the game state, depending on setup).
3. **First Action:** A short tutorial sequence begins automatically.
The piano keys on screen light up one at a time at 0.25x speed, clearly demonstrating what to do.
Players observe and start tapping the corresponding foil pads in sync.
4. **Main Interaction:** A short tutorial sequence begins automatically.
The piano keys on screen light up one at a time at 0.25x speed, clearly demonstrating what to do.
Players observe and start tapping the corresponding foil pads in sync.
5. **System Response:** The system provides immediate feedback to reinforce learning and engagement. A correct tap produces the corresponding piano note and progresses the sequence, while an incorrect tap triggers an error sound and resets the sequence to the beginning.
6. **Win / Lose / End Condition:** Each level completion is marked by a visual flash on the screen. Finishing the final advanced level signifies the end of the full interaction cycle and gives the player a clear sense of completion. After successfully completing the tutorial, the experience transitions into the main level at 0.75x speed, increasing the pace and challenge. Upon completing this level, the player unlocks the advanced level at full 1x speed, creating a clear sense of progression and mastery.
7. **Reset:** Once the final level is completed, any touch input resets the system instantly. The game returns to the tutorial phase, allowing new or returning players to begin the experience again seamlessly.

## 4.4 Rules of Play
If your project is a game, list the rules clearly.

- Tap the pad that corresponds to the currently glowing key on screen.
- Tapping any other pad counts as a wrong move.
- A wrong move resets the sequence to the beginning — no partial credit.
- Players cannot share tapping freely — there is an assigned pad per player.
- The goal is to complete the full song sequence without a single wrong tap.



---

# 5. Definition of Success

## 5.1 Definition of “Playable”
Your project will be considered complete only if these conditions are met.

- [ ]  All 8 foil pads reliably detect finger touch and send the correct signal to the ESP32
- [ ]  The ESP32 correctly identifies which pad was touched and sends the signal to the laptop via USB serial
- [ ]  The Python script on the laptop correctly plays the corresponding piano note on a correct touch
- [ ]  The Python script plays an error sound and resets the sequence on a wrong touch
- [ ]  The screen display shows keys lighting up in song sequence and is spatially aligned with the physical pads
- [ ]   At least one full song sequence can be completed without system failure


## 5.2 Minimum Viable Version
What is the smallest version of this project that still delivers the core experience?

**Response:**  
A working version where at least 4 of the 8 pads function, the screen shows which key to tap, a correct tap plays a note, and a wrong tap resets, even if only one song is loaded and the build finish is rough.

## 5.3 Stretch Features
What features are nice to have but not essential?

- `[Stretch feature 1]`
- `[Stretch feature 2]`
- `[Stretch feature 3]`

---

# 6. System Overview

## 6.1 Project Type
Check all that apply.

- [ ] Electronics-based
- [ ] Mechanical
- [*] Sensor-based
- [*] App-connected
- [ ] Motorized
- [ ] Sound-based
- [ ] Light-based
- [ ] Screen/UI-based
- [ ] Fabricated structure
- [ ] Game logic based
- [*] Installation / tabletop experience
- [ ] Other: `[Write here]`

## 6.2 High-Level System Description
Explain how the system works in simple terms.

Include:
- input,
- processing,
- output,
- physical structure,
- app interaction if any.

**Response:**  
`[Write here]`

## 6.3 Input / Output Map

| System Part | Type | What It Does |
|---|---|---|
| `[Button / Sensor / Switch / App Input]` | Input | `[Describe]` |
| `[ESP32 / Controller]` | Processing | `[Describe]` |
| `[LED / Motor / Servo / Buzzer / Display]` | Output | `[Describe]` |
| `[Mechanical Assembly]` | Physical Action | `[Describe]` |

---

# 7. Sketches and Visual Planning

## 7.1 Concept Sketch
Add an early sketch of the full idea.

**Insert image below:**  
`[Upload image and link here]`

Example:
```md

```

## 7.2 Labeled Build Sketch
Add a sketch with labels showing:
- structure,
- electronics placement,
- user touch points,
- moving parts,
- output elements.

**Insert image below:**  
`[Upload image and link here]`

## 7.3 Approximate Dimensions

| Dimension | Value |
|---|---|
| Length | `[Write here]` |
| Width | `[Write here]` |
| Height | `[Write here]` |
| Estimated weight | `[Write here]` |

---

# 8. Mechanical Planning

## 8.1 Mechanical Features
Check all that apply.

- [ ] Gears
- [ ] Pulleys
- [ ] Belt drives
- [ ] Linkages
- [ ] Hinges
- [ ] Shafts
- [ ] Springs
- [ ] Bearings
- [ ] Wheels
- [ ] Sliders
- [ ] Levers
- [*] Not applicable

## 8.2 Mechanical Description
Describe the mechanism and what it is meant to do.

**Response:**  
This project has no moving mechanical parts. The physical structure is static — MDF board with cutout windows, foamboard pads sitting in those windows, and an enclosed box underneath housing electronics. All interaction is through touch only.

## 8.3 Motion Planning
If something moves, explain:
- what moves,
- what causes the movement,
- how far it moves,
- how fast it moves,
- what could go wrong.

**Response:**  
Not applicable. Nothing moves in this project. The only "motion" is the player's hand touching a pad.

## 8.4 Simulation / CAD / Animation Before Making
If your project includes mechanical motion, document the digital planning before fabrication.

| Tool Used | File / Link | What Was Tested |
|---|---|---|
| Adobe Illustrator |  https://github.com/RishaSalunkhe/ODT2026-ProjectManagementTemplate/blob/main/images/Illustrator%20screenshot.png | Made the digital file to be laser cut as that was the best option due to accuracy of measurement, and more efficiency |
 
## 8.5 Changes After Digital Testing
What changed after the CAD, animation, or simulation stage?

**Response:**  
Not applicable — no CAD modelling used. All dimensions validated by physical measurement and paper sketch before MDF was cut.

---

# 9. Electronics Planning

## 9.1 Electronics Used

| Component | Quantity | Purpose |
|---|---:|---|
| ESP32 WROOM-32 DevKit| 1 | Main controller — reads capacitive touch, sends serial data to laptop |
| USB cable (micro-USB) | 1 |Powers ESP32 and carries serial data to laptop |
| Insulated copper wires | 8 | Connect to touchpads |
| Pin wires | 8 | For establishing connection with ESP32 |

## 9.2 Wiring Plan
Describe the main electrical connections.

**Response:**  
`[Write here]`

## 9.3 Circuit Diagram
Insert a hand-drawn or software-made circuit diagram.

**Insert image below:**  
`[Upload image and link here]`

## 9.4 Power Plan

| Question | Response |
|---|---|
| Power source | USB (micro-USB from laptop to ESP32) |
| Voltage required | `[Write here]` |
| Current concerns | `[Write here]` |
| Safety concerns | `[Write here]` |

---

# 10. Software Planning

## 10.1 Software Tools

| Tool / Platform | Purpose |
|---|---|
| MIT App Inventor | `[Purpose]` |
| Thonny- Micropython | `[Purpose]` |

## 10.2 Software Logic
Describe what the code must do.

Include:
- startup behavior,
- input handling,
- sensor reading,
- decision logic,
- output behavior,
- communication logic,
- reset behavior.

**Response:**  
`[Write here]`

## 10.3 Code Flowchart
Insert a flowchart showing your code logic.

Suggested sequence:
- start,
- initialize,
- wait for input,
- read input,
- decision,
- trigger output,
- repeat or reset,
- error handling.

**Insert image below:**  
`[Upload image and link here]`

## 10.4 Pseudocode

START
Initialize 8 touch pins
Connect ESP32 to WiFi hotspot
Set retval = "0"

LOOP:
    Read all 8 touch pin values
    If pin value < 200:
        Set retval = corresponding note letter
    Process app request
    Return retval to app
    Reset retval to "0"
    Wait 0.05 seconds

APP SIDE:
Every 100ms, call Web.Get to ESP32 IP
When response received:
    If response = "a" → play D4.mp3
    If response = "b" → play Dsharp.mp3
    ... and so on for all 8 notes
```

---

# 11. MIT App Inventor Plan

## 11.1 Is an app part of this project?
- [ ] Yes
- [ ] No

If yes, complete this section.

## 11.2 Why is the app needed?
Explain what the app adds to the experience.

Examples:
- remote control,
- score tracking,
- mode selection,
- personalization,
- triggering effects,
- displaying data.

**Response:**  
`[Write here]`

## 11.3 App Features

| Feature | Purpose |
|---|---|
| `[Bluetooth connect button]` | `[Purpose]` |
| `[Score display]` | `[Purpose]` |
| `[Control button / slider / label]` | `[Purpose]` |

## 11.4 UI Mockup
Insert a sketch or screenshot of the app interface.

**Insert image below:**  
`[Upload image and link here]`

## 11.5 App Screen Flow

1. `[Step 1]`
2. `[Step 2]`
3. `[Step 3]`
4. `[Step 4]`

---

# 12. Bill of Materials

## 12.1 Full BOM

| Item | Quantity | In Kit? | Need to Buy? | Estimated Cost | Material / Spec | Why This Choice? |
|---|---:|---|---|---:|---|---|
| ESP32 WROOM-32 DevKit |1| Yes | Yes | 599 | SquadPixel ESP-WROOM-32, 38-pin | Has 8 built-in capacitive touch pins, no external sensor IC needed |
| MDF board | 1 | No | No | `[Cost]` | `[Spec]` | `[Reason]` |
| `[Item]` | `[Qty]` | `[Yes/No]` | `[Yes/No]` | `[Cost]` | `[Spec]` | `[Reason]` |

## 12.2 Material Justification
Explain why you selected your main materials and components.

Examples:
- Why acrylic instead of cardboard?
- Why MDF instead of 3D print?
- Why servo instead of DC motor?
- Why bearing instead of a plain shaft hole?

**Response:**  
Aluminium foil over copper sheet or metal plates: Foil is cheap, available immediately, and wraps cleanly around foamboard. The ESP32's capacitive sensing is sensitive enough to detect touch through foil perfectly well. Metal plates would be more durable but cost more and require drilling or adhesive mounting.
MDF over plywood or 3D print: MDF cuts cleanly with a jigsaw and gives precise rectangular cutout windows. It is flat, paintable, and available at any hardware store. 3D printing would take too long and not give the required rigidity at this size.
USB serial over Bluetooth: Wired USB is more reliable for a live exhibition — no pairing issues, no dropout, no latency. Bluetooth would add unnecessary complexity for a first build.

## 12.3 Items to Purchase Separately

| Item | Why Needed | Purchase Link | Latest Safe Date to Procure | Status |
|---|---|---|---|---|
| ESP32 WROOM-32 | `[Reason]` | `[Link]` | `[Date]` | `[Pending / Ordered / Received]` |
| `[Item]` | `[Reason]` | `[Link]` | `[Date]` | `[Pending / Ordered / Received]` |

## 12.4 Budget Summary

| Budget Item | Estimated Cost |
|---|---:|
| Electronics | 599 |
| Mechanical parts | `[Cost]` |
| Fabrication materials | `[Cost]` |
| Purchased extras | `[Cost]` |
| Contingency | `[Cost]` |
| **Total** | 599 |

## 12.5 Budget Reflection
If your cost is too high, what can be simplified, removed, substituted, or shared?

**Response:**  
`[Write here]`

---

# 13. Planning the Work

## 13.1 Team Working Agreement
Write how your team will work together.

Include:
- how tasks are divided,
- how decisions are made,
- how progress will be checked,
- what happens if a task is delayed,
- how documentation will be maintained.

**Response:**  
`[Write here]`

## 13.2 Task Breakdown

| Task ID | Task | Owner | Estimated Hours | Deadline | Dependency | Status |
|---|---|---|---:|---|---|---|
| T1 | Finalise concept and game mechanic | Risha & Swaranjali | 6 | `[Date]` | `None` | `To Do` |
| T2 | Complete BOM and procure materials` | `[Name]` | `1` | `[Date]` | `T1` | `To Do` |
| T3 | Upload ESP32 sketch and test touch pins | `[Name]` | `2` | `[Date]` | `T1` | `To Do` |
| T4 | `[Build structure]` | `[Name]` | `4` | `[Date]` | `T1` | `To Do` |
| T5 | `[Write control code]` | `[Name]` | `4` | `[Date]` | `T3` | `To Do` |
| T6 | `[Integrate system]` | `[Name]` | `4` | `[Date]` | `T4, T5` | `To Do` |
| T7 | `[Playtest]` | `[Name]` | `2` | `[Date]` | `T6` | `To Do` |
| T8 | `[Refine and document]` | `[Name]` | `3` | `[Date]` | `T7` | `To Do` |

## 13.3 Responsibility Split

| Area | Main Owner | Support Owner |
|---|---|---|
| Concept and gameplay | Risha & Swaranjali | Risha & Swaranjali  |
| Electronics | `[Name]` | `[Name]` |
| Coding | Swaranjali | `[Name]` |
| App | Swaranjali | `[Name]` |
| Mechanical build | `[Name]` | `[Name]` |
| Testing | `[Name]` | `[Name]` |
| Documentation | Risha | Swaranjali |

---

# 14. Weekly Milestones

## 14.1 Four-Week Plan

### Week 1 — Plan and De-risk
Expected outcomes:
- [*] Idea finalized
- [*] Core interaction decided
- [ ] Sketches made
- [ ] BOM completed
- [ ] Purchase needs identified
- [*] Key uncertainty identified
- [ ] Basic feasibility tested

### Week 2 — Build Subsystems
Expected outcomes:
- [ ] Electronics tests completed
- [ ] CAD / structure planning completed
- [ ] App UI started if needed
- [ ] Mechanical concept tested
- [ ] Main subsystems partially working

### Week 3 — Integrate
Expected outcomes:
- [*] Physical body built
- [ ] Electronics integrated
- [ ] Code connected to hardware
- [ ] App connected if required
- [ ] First playable version exists

### Week 4 — Refine and Finish
Expected outcomes:
- [ ] Technical bugs reduced
- [ ] Playtesting completed
- [*] Improvements made
- [*] Documentation completed
- [*] Final build ready

## 14.2 Weekly Update Log

| Week | Planned Goal | What Actually Happened | What Changed | Next Steps |
|---|---|---|---|---|
| Week 1 | `[Write here]` | `[Write here]` | `[Write here]` | `[Write here]` |
| Week 2 | `[Write here]` | `[Write here]` | `[Write here]` | `[Write here]` |
| Week 3 | `[Write here]` | `[Write here]` | `[Write here]` | `[Write here]` |
| Week 4 | `[Write here]` | `[Write here]` | `[Write here]` | `[Write here]` |

---

# 15. Risks and Unknowns

## 15.1 Risk Register

| Risk | Type | Likelihood | Impact | Mitigation Plan | Owner |
|---|---|---|---|---|---|
| `[Example: Bluetooth disconnects]` | `Technical` | `Medium` | `High` | `[Fallback interaction / simplify connection flow]` | `[Name]` |
| `[Example: Structure breaks during play]` | `Mechanical` | `Medium` | `High` | `[Reinforce joints / change material]` | `[Name]` |
| `[Risk]` | `[Technical / Material / Time / Gameplay]` | `[Low/Medium/High]` | `[Low/Medium/High]` | `[Plan]` | `[Name]` |
| `[Risk]` | `[Type]` | `[Low/Medium/High]` | `[Low/Medium/High]` | `[Plan]` | `[Name]` |

## 15.2 Biggest Unknown Right Now
What is the single biggest uncertainty in your project at this stage?

**Response:**  
`[Write here]`

---

# 16. Testing and Playtesting

## 16.1 Technical Testing Plan

| What Needs Testing | How You Will Test It | Success Condition |
|---|---|---|
| `[Bluetooth connection]` | `[Method]` | `[What counts as success?]` |
| `[Mechanism movement]` | `[Method]` | `[What counts as success?]` |
| `[Sensor behavior]` | `[Method]` | `[What counts as success?]` |
| `[App communication]` | `[Method]` | `[What counts as success?]` |

## 16.2 Playtesting Plan

| Question | How You Will Check |
|---|---|
| Do players understand what to do?  | Watch first-time players — do they immediately tap the correct pad without instruction?|
| Is the interaction satisfying? | Ask players if the note felt connected to their touch or delayed |
| Do players want another turn? | Count how many players immediately try again after finishing or failing |
| Is the challenge balanced? | Check if the song sequence feels too fast or too slow, adjust timing in code |
| Is the response clear and immediate? | Ask players if they could immediately tell they hit the wrong pad |

## 16.3 Testing and Debugging Log

| Date | Problem Found | Type | What You Tried | Result | Next Action |
|---|---|---|---|---|---|
| `[Date]` | `[Describe issue]` | `[Technical / Mechanical / UI / Gameplay]` | `[What you did]` | `[Worked / Partly / Failed]` | `[Next step]` |
| `[Date]` | `[Describe issue]` | `[Type]` | `[What you did]` | `[Result]` | `[Next step]` |

## 16.4 Playtesting Notes

| Tester | What They Did | What Confused Them | What They Enjoyed | What You Will Change |
|---|---|---|---|---|
| `[Peer / friend / classmate]` | `[Observation]` | `[Observation]` | `[Observation]` | `[Action]` |
| `[Peer / friend / classmate]` | `[Observation]` | `[Observation]` | `[Observation]` | `[Action]` |

---

# 17. Build Documentation

## 17.1 Fabrication Process
Describe how the project was physically made.

Include:
- cutting,
- 3D printing,
- assembly,
- fastening,
- wiring,
- finishing,
- revisions.

**Response:**  
`[Write here]`

## 17.2 Build Photos
Add photos throughout the project.

Suggested images:
- early sketch,
- prototype,
- electronics testing,
- mechanism test,
- app screenshot,
- final build.

Example:
```md

https://github.com/RishaSalunkhe/ODT2026-ProjectManagementTemplate/blob/main/images/concept%20image.jpeg

```

## 17.3 Version History

| Version | Date | What Changed | Why |
|---|---|---|---|
| v1 | Week 1 | Single pad MicroPython test on bare ESP32 | Validate that capacitive touch sensing worked before committing to full build |
| v2 | Week 2 | MDF layout created digitally, foamboard pads assembled | First physical build complete |
| v3 | Week 3 | MDF cut and assembled, foil and wires stuck onto foambboard | First working end-to-end version
|  v4  |  Week 4 | Screen display setup, threshold tuning, final fixes | Exhibition-ready version
 
---

# 18. Final Outcome

## 18.1 Final Description
Describe the final version of your project.

**Response:**  
`[Write here]`

## 18.2 What Works Well
- `[Point 1]`
- `[Point 2]`
- `[Point 3]`

## 18.3 What Still Needs Improvement
- `[Point 1]`
- `[Point 2]`
- `[Point 3]`

## 18.4 What Changed From the Original Plan
How did the project change from the initial idea?

**Response:**  
`[Write here]`

---

# 19. Reflection

## 19.1 Team Reflection
What did your team do well?  
What slowed you down?  
How well did you manage time, tasks, and responsibilities?

**Response:**  
`[Write here]`

## 19.2 Technical Reflection
What did you learn about:
- electronics,
- coding,
- mechanisms,
- fabrication,
- integration?

**Response:**  
`[Write here]`

## 19.3 Design Reflection
What did you learn about:
- designing for play,
- delight,
- clarity,
- physical interaction,
- player understanding,
- iteration?

**Response:**  
`[Write here]`

## 19.4 If You Had One More Week
What would you improve next?

**Response:**  
`[Write here]`

---

# 20. Final Submission Checklist

Before submission, confirm that:
- [ ] Team details are complete
- [ ] Project description is complete
- [ ] Inspiration sources are included
- [ ] Player journey is written
- [ ] Sketches are added
- [ ] BOM is complete
- [ ] Purchase list is complete
- [ ] Budget summary is complete
- [ ] Mechanical planning is documented if applicable
- [ ] App planning is documented if applicable
- [ ] Code flowchart is added
- [ ] Task breakdown is complete
- [ ] Weekly logs are updated
- [ ] Risk register is complete
- [ ] Testing log is updated
- [ ] Playtesting notes are included
- [ ] Build photos are included
- [ ] Final reflection is written

---

# 21. Suggested Repository Structure

```text
project-repo/
├── README.md
├── images/
│   ├── concept-sketch.jpg
│   ├── labeled-sketch.jpg
│   ├── circuit-diagram.jpg
│   ├── ui-mockup.jpg
│   ├── prototype-1.jpg
│   └── final-build.jpg
├── code/
│   ├── main.py
│   ├── test_code.py
│   └── notes.md
├── cad/
│   ├── models/
│   └── screenshots/
└── docs/
    ├── references.md
    └── extra-notes.md
```

---

# 22. Instructor Review

## 22.1 Proposal Approval
- [ ] Approved to proceed
- [ ] Approved with changes
- [ ] Rework required before proceeding

**Instructor comments:**  
`[Instructor fills this section]`

## 22.2 Midpoint Review
`[Instructor fills this section]`

## 22.3 Final Review Notes
`[Instructor fills this section]`
