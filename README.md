# Learning that LASTS (LtL) — Course Builder

An AI-powered course design toolkit for building and delivering training using the **Dialogue Education / Learning that LASTS (LtL)** framework.

This system transforms the way training is designed—from brainstorming to delivery—by ensuring that learners do the thinking, not just listen to content.

---

## 🎯 What is Learning that LASTS?

**Learning that LASTS** (also called Dialogue Education) is an adult education framework that recognizes a fundamental truth: **adults learn through dialogue and practice, not lectures.**

The framework guides trainers to ask powerful questions rather than deliver information, and to design learning tasks (not presentations) where participants actively construct knowledge and apply it to their work.

---

## 📊 The LtL Workflow

This toolkit breaks training development into five sequential stages:

```
Stage 1: Brainstorming        (/ltl-brainstorming)
    ↓
Stage 2: Event Design          (/ltl-event)
    ↓
Stage 3: Module Design (×N)    (/ltl-module <title>)
    ↓
Stage 4: Generate Outputs      (/ltl-generate)
```

An orchestrator skill (`/ltl`) guides you through the journey, showing you where you are and what to do next.

---

## 🚀 Quick Start

### Prerequisites
- An AI-assisted IDE that supports workspace prompts (e.g., Cursor, Windsurf, or VS Code with GitHub Copilot)
- A workspace for your training project

### Installation

Since the skills are stored in the `.prompts` directory, compatible AI IDEs will automatically detect them. There is no need to install them globally.

1. **Open this repository**
   - Open the folder containing the `.prompts` directory in your AI IDE (Cursor, Windsurf, or VS Code).

2. **Create a training project workspace** (or use an existing one):
   - Create directories: `overview-session/`, `training-modules/`, `ltl-resources/`

3. **Start the journey:**
   - In your AI chat interface, run `/ltl` to begin

---

## 📖 How It Works

### Stage 1 — Brainstorming (`/ltl-brainstorming`)

**Purpose**: Gather your raw ideas and materials before formal design.

**What it does**:
- Scans your workspace for existing training materials (curriculum, slides, notes)
- Interviews you through 7 open-ended questions about your training vision
- Produces `overview-session/brainstorming-notes.md` to seed the next stage

**Example output**: A document with your training's core idea, intended participants, dream outcome, suggested modules, and risks.

---

### Stage 2 — Event Design (`/ltl-event`)

**Purpose**: Design the complete training event using the LtL Event Design Guide.

**What it does**:
- Walks you through 7 structured questions (WHO, WHY, WHAT EVIDENCE, WHERE, HOW MUCH, WHEN, HOW)
- Generates `overview-session/overview.md` with a full module list, timing, and logistics
- Uses your brainstorming notes to pre-fill suggestions

**Example output**: A complete event overview with participants, facilitators, goals, module titles/times, and a status table.

---

### Stage 3 — Module Design (`/ltl-module <Module Title>`)

**Purpose**: Design each module individually using the LtL Module Design Guide.

**What it does**:
- Interviews you about WHO, WHY, WHAT EVIDENCE, WHERE, WHEN for each module
- Guides you through the **5 Cs** — Connection, Content, Challenge, Change, Closure
- Converts each C into actionable **Learning Tasks** (with time, task, resource, and ASK domain)
- Generates two files per module:
  - **Full design** (`<module-slug>.md`) — complete reference for facilitators
  - **Facilitator summary** (`<module-slug>-summary.md`) — one-page cheat sheet

**Example output**: A structured module with learning objectives, tasks for each phase, timing, and facilitator notes.

---

### Stage 4 — Generate Outputs (`/ltl-generate [output-type|all]`)

**Purpose**: Generate all final training materials from your module designs.

**What it does**:
- Reads all completed module files
- Generates 8 types of outputs (see below)
- Writes all files to `training-materials/` with proper organization

**Output types**:
1. **Participant Handouts** — Task instructions for learners
2. **Quizzes** — Tests tied to learning objectives (with answer key)
3. **Participant Workbook** — Combined module tasks + action plan
4. **Assignments** — Follow-up tasks for post-training application
5. **Teacher's Handbook** — Facilitation scripts, timing cues, troubleshooting
6. **Teaching Props Lists** — Prep checklists and timelines
7. **Image Generation Prompts** — Ready-to-paste prompts for AI image tools
8. **Presentation Prompts** — Slide-by-slide outlines for AI slide generators

**Example usage**:
```
/ltl-generate handouts              # Generate just handouts
/ltl-generate quiz                  # Generate just quizzes
/ltl-generate teacher handbook      # Generate facilitator handbook
/ltl-generate all                   # Generate everything
```

---

## 📁 Workspace Structure

When you use the system, it creates and maintains this structure:

```
your-project/
├── overview-session/
│   ├── overview.md                 # Main event design (generated by /ltl-event)
│   └── brainstorming-notes.md      # Raw ideas (generated by /ltl-brainstorming)
├── training-modules/
│   ├── module-1-slug/
│   │   ├── module-1-slug.md        # Full module design
│   │   └── module-1-slug-summary.md # Facilitator summary
│   ├── module-2-slug/
│   │   ├── module-2-slug.md
│   │   └── module-2-slug-summary.md
│   └── ...
├── training-materials/            # Generated outputs
│   ├── handouts/
│   ├── quizzes/
│   ├── workbook/
│   ├── assignments/
│   ├── teacher-handbook/
│   ├── props/
│   └── prompts/
├── ltl-resources/                 # Your input materials (optional)
│   ├── Module Design Guide.docx
│   ├── Event Design Guide.docx
│   └── ... (your existing curriculum)
└── .gitignore                     # Git ignore patterns (optional)
```

---

## 🎓 Core Concepts

### The 6 Sections (Module Design)

Each module is designed around **6 sections**:

1. **WHO** — Describe the learners and facilitators
2. **WHY** — Explain the "Before Picture" (the gap this module addresses)
3. **WHAT EVIDENCE** — Define the "After Picture" (learning, transfer, impact)
4. **WHERE** — Describe the location and setup
5. **WHEN** — Specify duration and sequence
6. **HOW** — Design the 5 Cs as Learning Tasks

### The 5 Cs (Learning Flow)

Each module flows through **5 learning segments**:

1. **Connection** — Hook participants to the topic (5–10 min)
2. **Content** — Introduce new concepts (active learning, not lecture)
3. **Challenge** — Apply content to a realistic problem
4. **Change** — Reflect and commit to new actions
5. **Closure** — Summarize and celebrate learning

### Learning Tasks

Each C is broken into **Learning Tasks** with four elements:

| Time | Task | Resource | ASK Domain |
|------|------|----------|------------|
| 10 min | *Participants discuss...* | Case study handout | **Skill** |

- **Time**: Allocated duration
- **Task**: What participants DO (in imperative)
- **Resource**: Tools, materials, or people needed
- **ASK Domain**: Does this develop Attitude, Skill, or Knowledge?

---

## 💡 Design Principles

The system enforces these principles throughout:

✅ **The learner does the thinking** — Tasks are designed so participants solve problems, not listen to answers

✅ **One question at a time** — Skills never ask multiple questions in one turn

✅ **Suggest answers** — Every question comes with a thinking prompt

✅ **Evaluate then polish** — Before moving on, AI identifies gaps and polishes answers with the trainer

✅ **Write files, don't display** — All outputs are written to your workspace, not just shown

✅ **Build on existing materials** — If you have curriculum docs, they are analyzed and reused

---

## 🛠️ Skills Reference

### `/ltl` (Orchestrator)
- Greets you by name (asks how to address you)
- Shows project status (which stages are complete)
- Tells you exactly what to run next
- Never does the detailed work—just routes and checks progress

### `/ltl-brainstorming`
- Explores your raw ideas and existing materials
- Asks 7 open-ended questions about your training vision
- Synthesizes and flags tensions
- Generates `brainstorming-notes.md`

### `/ltl-event`
- Guides you through the 7-question Event Design Guide
- Pre-fills suggestions from brainstorming notes
- Generates `overview.md` with event details and module list
- Marks modules as "Not started" (ready for design)

### `/ltl-module <Title>`
- Designs one module at a time
- Pre-fills context from event overview
- Guides through 6 sections + 5 Cs
- Converts content into Learning Tasks
- Generates full design + facilitator summary
- Updates module status to "Complete"

### `/ltl-generate [output-type|all]`
- Reads all completed modules
- Generates 8 types of training materials
- All outputs reflect LtL principles (task-focused, not content-focused)
- Writes files to `training-materials/`

---

## 📝 Examples

### Example: Designing a NotebookLM Module

```
User: /ltl-module NotebookLM
AI: We'll be designing **NotebookLM** (Module 2 of 5, 75 min). Let's begin.

AI: **Section 1 — WHO**
The event overview describes your learners as "Bible translators, mixed tech experience". 
Is there anything specific about this module that changes who you're designing for?

User: Same audience, but I want to highlight that most are skeptical of AI.

AI: Got it — you're designing for a skeptical audience who needs to see how NotebookLM 
saves time without replacing human judgment. I've noted that.

AI: **Section 2 — WHY**
Why is this NotebookLM module needed? What specific gap does it address?

User: Right now they manually summarize source texts. This is time-consuming and error-prone.
```

And so on—one question at a time, building the design interactively.

---

## 🔧 Customization & Extension

Each `.prompt.md` file is a complete AI skill. You can:

1. **Edit the prompts directly** — Add organization-specific instructions or adjust tone
2. **Use in other tools** — Any AI chat supporting prompt files can use these
3. **Extend the workflow** — Add intermediate review steps or specialized skills
4. **Integrate with other systems** — Export designs to Notion, Miro, or other tools

---

## 📚 Resources

### About Learning that LASTS / Dialogue Education
- **Vella, Jane** (1994). *Learning to Listen, Learning to Teach* (foundational text)
- **Knowles, Malcolm** (1984). *Andragogy in Action* (adult learning principles)

### The Event & Module Design Guides
This toolkit implements the LtL **Event Design Guide** (7 questions) and **Module Design Guide** (6 sections + 5 Cs), validated through NLCI training programs.

---

## 🤝 Contributing

This toolkit is designed for iteration. If you:
- Find missing prompts or instructions
- Want to add new output types
- Have examples of excellent module designs
- Discover bugs or unclear guidance

Please open an issue or PR on the GitHub repo.

---

## 📄 License

[Add license info here]

---

## 🎯 Get Started

1. Open this repository in your AI IDE
2. Create or open a training project workspace
3. Run `/ltl` in your AI chat to initialize
4. Follow the guided workflow

**That's it.** You're now designing training the LtL way.

---

## Questions?

Refer to the individual skill files in `/.prompts` for detailed instructions on each step, or run any skill with `/ltl` to get oriented.
