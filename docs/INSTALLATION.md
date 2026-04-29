# LtL Course Builder — Installation & Setup

## System Requirements

- **VS Code** with **GitHub Copilot Chat**
- **Git** (for version control and pushing to GitHub)
- A terminal or command line (PowerShell, bash, zsh, etc.)

## Installation Steps

### 1. Copy Skills to Your Prompts Directory

**Windows:**
```powershell
Copy-Item "path/to/ltl-course-builder/skills/*.prompt.md" `
  -Destination "$env:APPDATA\Code\User\prompts\" -Verbose
```

**macOS/Linux:**
```bash
cp path/to/ltl-course-builder/skills/*.prompt.md \
   ~/Library/Application\ Support/Code/User/prompts/
```

Verify: You should now see `/ltl`, `/ltl-brainstorming`, `/ltl-event`, `/ltl-module`, `/ltl-generate` available in Copilot chat.

---

### 2. Create Your Training Project Workspace

Create a new folder for your training project:

```bash
mkdir my-training-project
cd my-training-project
```

Create the required subdirectories:

```bash
mkdir -p overview-session training-modules ltl-resources training-materials
```

---

### 3. (Optional) Initialize Git

If you plan to version control or push to GitHub:

```bash
git init
git config user.name "Your Name"
git config user.email "your.email@example.com"
```

Create a `.gitignore` file to exclude non-essential files:

```
# Node (if using Node tools)
node_modules/
*.log

# OS files
.DS_Store
Thumbs.db

# IDE
.vscode/
*.swp
*.swo

# Generated outputs (optional: keep or remove based on preference)
# training-materials/

# Temporary files
*.tmp
*.bak
```

Add and commit:

```bash
git add .
git commit -m "Initial project setup"
```

---

### 4. Start Your First Training Design

Open VS Code in your training project folder:

```bash
code .
```

Open GitHub Copilot Chat and run:

```
/ltl
```

The `/ltl` orchestrator will greet you, ask your name, and guide you through the workflow.

---

## Typical Workflow

```
Session 1: Brainstorm
  /ltl-brainstorming
  → Produces: overview-session/brainstorming-notes.md

Session 2: Event Design  
  /ltl-event
  → Produces: overview-session/overview.md

Session 3+: Module Design (repeated for each module)
  /ltl-module "Module 1"
  /ltl-module "Module 2"
  /ltl-module "Module 3"
  → Produces: training-modules/<slug>/<slug>.md + summary

Final Session: Generate Outputs
  /ltl-generate all
  → Produces: training-materials/* (handouts, quizzes, handbook, etc.)
```

---

## Pushing to GitHub

Once you've completed your training design, push it to a GitHub repo:

```bash
# Add remote (replace with your actual repo URL)
git remote add origin https://github.com/nlci-lab/your-training.git

# Stage all changes
git add .

# Commit
git commit -m "Completed training design: [Event Name]"

# Push to main branch (use 'gh' or 'git')
git push -u origin main
```

---

## File Structure Reference

After running all stages, you'll have:

```
my-training-project/
├── README.md                          (Your project notes)
├── .git/                              (Version control)
├── .gitignore                         (Git ignore patterns)
│
├── overview-session/
│   ├── brainstorming-notes.md        (Stage 1 output)
│   └── overview.md                    (Stage 2 output)
│
├── training-modules/
│   ├── module-1/
│   │   ├── module-1.md               (Stage 3 output)
│   │   └── module-1-summary.md       (Facilitator summary)
│   ├── module-2/
│   │   ├── module-2.md
│   │   └── module-2-summary.md
│   └── ...
│
├── ltl-resources/                    (Your input files)
│   ├── curriculum.docx
│   ├── slides.pptx
│   └── ...
│
└── training-materials/               (Stage 4 outputs)
    ├── handouts/
    ├── quizzes/
    ├── workbook/
    ├── assignments/
    ├── teacher-handbook/
    ├── props/
    └── prompts/
```

---

## Troubleshooting

### "Skill not found" error
**Solution**: Verify that all `.prompt.md` files are in your VS Code prompts directory. Reload VS Code and try again.

### Skills are loaded but responses are generic
**Solution**: Check that the skill file content matches what's in this repo. AI behavior depends on the exact prompt instructions.

### Git push authentication fails
**Solution**: 
- Use `gh` (GitHub CLI) if available: `gh auth login`
- Or use SSH keys: `ssh-keygen -t ed25519 -C "your.email@example.com"`
- Or use a GitHub Personal Access Token

---

## Next Steps

1. ✅ Install skills
2. ✅ Create project folder
3. ✅ (Optional) Initialize git
4. ▶️ **Run `/ltl` to begin your training design**

Happy designing!
