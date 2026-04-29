# Background & Context — LtL Course Builder

## The Problem

For decades, training has followed a predictable pattern: **experts deliver content, and participants take notes.** This model assumes that information transfer equals learning—a premise contradicted by decades of adult education research.

The result? Participants forget most of what they heard. Transfer to the workplace is rare. Training budgets are spent inefficiently.

---

## The Solution: Dialogue Education

**Learning that LASTS (LtL)**, also called **Dialogue Education**, is a proven framework for adult learning developed and refined through decades of international development work. It's based on a simple insight:

> **Adults learn through dialogue and practice, not lectures.**

When trainers ask powerful questions instead of delivering answers, and when participants *do* the thinking (solving problems, applying concepts, teaching each other), learning sticks.

### The Core Principle

Instead of:
```
Trainer talks → Participant listens → Participant forgets
```

Do this:
```
Trainer asks → Participants think & discuss → Participants practice → Transfer happens
```

---

## Why This Toolkit?

LtL is powerful, but **designing training this way is complex**. It requires:

- Asking the right interview questions to surface the real need
- Structuring content as *tasks*, not lectures
- Mapping learning outcomes to evidence and practice
- Managing multiple decision points (Who? Why? What Evidence? Where? When? How?)
- Generating polished materials that reflect the design

Trainers often end up doing this manually, consulting guides, and working alone. The process is error-prone and can take weeks.

**This toolkit automates the guided interview and file generation**, keeping trainers focused on *thinking* rather than *typing*.

---

## The NLCI Origin Story

This toolkit was born in the context of **NLCI (Nigeria Lingua Language Center)** and international Bible translation training.

### The Scenario

NLCI trains Bible translators, linguistic specialists, and community literacy workers—often in resource-constrained contexts (limited internet, multiple languages, mixed tech literacy).

**The Challenge:**
- Existing training was content-heavy (readings, lectures)
- Participants had highly varied background knowledge
- Limited time (1–3 day events)
- High stakes (translation quality affects communities)

**The Opportunity:**
- A dedicated, experienced training team
- Clear learning goals (participants must apply concepts immediately)
- A framework (LtL) proven to work with this exact audience
- A need to scale training to multiple sites and languages

### The Process

Rather than design everything by hand, the NLCI training team adopted a systematic approach:

1. **Document the design process** — Codify the Event Design Guide and Module Design Guide
2. **Identify the workflow** — Brainstorm → Event Design → Module Design → Outputs
3. **Automate the interviews** — Build AI prompts that guide each stage
4. **Generate materials** — Produce handouts, quizzes, handbooks automatically
5. **Iterate and refine** — Learn from each training, improve the system

The result: **trainers could design a 2-day multi-module event in ~8 hours**, instead of weeks of solo work.

---

## Design Philosophy

This toolkit reflects several key values:

### 1. **The Trainer is the Expert**
The AI prompts *interview* the trainer, but the trainer decides. AI suggests, confirms, and polishes—it doesn't replace human judgment.

### 2. **One Question at a Time**
Overwhelm kills thinking. Every prompt asks exactly one question, with a suggested answer to prime thinking.

### 3. **Write Files, Don't Display Content**
All outputs go into the trainer's workspace as actual files, ready to use. No copy-pasting from chat windows.

### 4. **Build on What Exists**
The toolkit scans the workspace for existing materials, analyzes them, and reuses them—respecting work already done.

### 5. **Keep the Learner Doing the Thinking**
Every generated task, quiz, and handout is designed to *engage* participants, not just inform them.

### 6. **Iterate Openly**
The toolkit is meant to evolve. Each training produces feedback that improves the next design.

---

## The Five-Stage Workflow

The toolkit breaks training development into five sequential, manageable stages:

### Stage 1 — Brainstorming (`/ltl-brainstorming`)

**Inputs:** Your raw ideas, existing materials, hunches about what's needed

**Process:** Interview-style questions to surface the vision, audience, constraints, and risks

**Output:** `brainstorming-notes.md` — Your thinking, documented

**Why this stage?** Before formal design, get your ideas out of your head and into a document. Capture the "why" before you design the "what."

---

### Stage 2 — Event Design (`/ltl-event`)

**Inputs:** Brainstorming notes, any existing event plans

**Process:** 7-question Event Design Guide (WHO, WHY, WHAT EVIDENCE, WHERE, HOW MUCH, WHEN, HOW)

**Output:** `overview.md` — Complete event blueprint with module list

**Why this stage?** You need clarity on the whole event before designing individual modules. This stage forces you to think about scope, timing, and participant expectations upfront.

---

### Stage 3 — Module Design (`/ltl-module`) [Repeated for each module]

**Inputs:** Event overview, existing content for that module

**Process:** 6-section Module Design Guide + 5 Cs (Connection, Content, Challenge, Change, Closure)

**Output:** Full module design + facilitator summary

**Why this stage?** Each module gets its own interview. This keeps module complexity manageable and ensures consistent quality across the event.

---

### Stage 4 — Generate Outputs (`/ltl-generate`)

**Inputs:** All completed module designs

**Process:** Read all modules and generate 8 output types (handouts, quizzes, workbook, assignments, etc.)

**Output:** `training-materials/` folder with polished, ready-to-use files

**Why this stage?** Once the design is locked, generating materials is mechanical. Automate it.

---

### Stage 5 — Navigation (`/ltl`)

**Inputs:** Current state of the project (reading .md files)

**Process:** Show the trainer where they are and what to do next

**Output:** Clear next steps

**Why this stage?** Long workflows are confusing. An orchestrator skill keeps you oriented.

---

## Key Concepts

### The 6 Sections (Module Design)

Every module is designed around these six lenses:

1. **WHO** — Who is learning? Who is teaching?
2. **WHY** — What gap or problem does this module address?
3. **WHAT EVIDENCE** — What will participants do differently after? (Learning, Transfer, Impact)
4. **WHERE** — Where does this happen? What's the physical/digital setup?
5. **WHEN** — How long? When in the sequence?
6. **HOW** — What are the learning tasks? (Structured through 5 Cs)

### The 5 Cs (Learning Flow)

Every module flows through five learning segments:

1. **Connection** (5–10 min) — Hook participants. Why does this matter?
2. **Content** (15–25 min) — Introduce concepts through *tasks*, not lectures
3. **Challenge** (20–30 min) — Apply concepts to a realistic problem
4. **Change** (10–15 min) — Reflect. What will you do differently?
5. **Closure** (5–10 min) — Celebrate. Look ahead.

### Learning Tasks

The core unit is the **Learning Task**:

| Time | Task | Resource | ASK Domain |
|------|------|----------|------------|
| 10 min | *Participants work in pairs to identify three concepts from the text that apply to their translation* | Bible passage handout, concept checklist | **Skill** |

Every task has:
- **Time** — How long?
- **Task** — What do participants *do*? (Imperative verb: discuss, analyze, practice, etc.)
- **Resource** — What tools or materials do they use?
- **ASK** — Does this develop **A**ttitude, **S**kill, or **K**nowledge?

---

## The Output Types

Once modules are designed, the toolkit generates 8 types of training materials:

1. **Participant Handouts** — Task instructions, reflection space
2. **Quizzes** — Formative + summative assessments tied to learning objectives
3. **Participant Workbook** — Combined module tasks + action plan (whole event)
4. **Assignments** — Real-world follow-up tasks (post-training application)
5. **Teacher's Handbook** — Facilitation scripts, timing cues, troubleshooting
6. **Teaching Props Lists** — Physical setup, materials prep, timeline
7. **Image Generation Prompts** — Ready-to-paste prompts for DALL-E / Midjourney
8. **Presentation Prompts** — Slide-by-slide outlines for AI slide tools

All outputs reflect LtL principles: **task-focused, participant-centered, evidence-based.**

---

## Evolution & Lessons

### What Worked

✅ **Structured interviews** — Trainers appreciated being asked one question at a time  
✅ **Suggested answers** — Priming questions with suggestions accelerated thinking  
✅ **File-based outputs** — Having actual files in the workspace, not chat display, was essential  
✅ **Materials analysis** — Analyzing existing content before the interview saved time  
✅ **Modular design** — One module at a time prevented overwhelm  

### What Evolved

- Added **Phase 0** (materials analysis) to brainstorming, event, and module skills
- Clarified the **5 Cs** structure for consistency across events
- Formalized the **Learning Tasks** format (time | task | resource | ASK)
- Expanded **output types** from basic handouts to 8 specialized formats
- Created the **orchestrator skill** (/ltl) to keep trainers oriented

### What's Still Experimental

- How to handle multi-language training designs
- How to template customizable outputs (e.g., "this handout works for 20 people OR 5 people")
- Integration with learning management systems (Notion, Miro, etc.)
- Real-time collaboration on module design (multiple facilitators)

---

## Who This Is For

**This toolkit is designed for:**
- ✅ Experienced trainers wanting to scale LtL-based training
- ✅ Training teams designing multi-module events
- ✅ Organizations building repeatable training programs
- ✅ International development orgs training across multiple sites/languages
- ✅ Anyone who believes adults learn through dialogue, not lectures

**This toolkit is NOT designed for:**
- ❌ One-off workshops (overkill for single-session training)
- ❌ Lectures that must remain content-heavy (conflicts with LtL philosophy)
- ❌ Fully asynchronous online training (works better with live facilitation)

---

## Contributing & Evolution

This toolkit was born from NLCI's training practice. It's meant to evolve:

- Have you used it? What worked? What didn't?
- Better prompts? Different output formats? Language-specific guides?
- Examples from other training contexts? (Healthcare, tech, nonprofit, etc.)

**Open an issue. Share a PR. Build on this work.**

---

## Resources & References

### Key Texts
- **Vella, Jane** (1994). *Learning to Listen, Learning to Teach* — Foundational LtL text
- **Knowles, Malcolm** (1984). *Andragogy in Action* — Adult learning principles
- **Merriam & Bierema** (2013). *Adult Learning* — Research summary

### The NLCI Context
- [NLCI Website](https://nlci.org.ng) — Nigeria Lingua Language Center
- LtL is used in Bible translation, linguistic training, and community literacy programs

### This Toolkit
- Created: 2026
- Maintained by: NLCI Training Team
- GitHub: github.com/nlci-lab/ltl-course-builder

---

## A Note on AI & Design

This toolkit uses AI to **automate the interview and file generation**, not to *replace* the designer's thinking.

The AI:
- ✅ Asks structured questions
- ✅ Suggests answers based on context
- ✅ Identifies gaps and inconsistencies
- ✅ Generates polished files

The trainer:
- ✅ Decides the content and direction
- ✅ Judges the quality of suggestions
- ✅ Confirms or corrects every answer
- ✅ Owns the final design

**The trainer remains the expert.** AI is the structured interview partner.

---

## Getting Started

1. Copy the skill files to your VS Code prompts folder (see INSTALLATION.md)
2. Create a training project workspace
3. Run `/ltl` to begin
4. Follow the guided workflow

The toolkit does the heavy lifting. You focus on the thinking.

**Ready?** Go design a training that actually changes behavior. 🚀
