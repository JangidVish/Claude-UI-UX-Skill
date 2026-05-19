# UI/UX Agency Skill System

A complete AI-assisted UI/UX workflow for web agencies. Each skill handles one phase of the project and saves its output to `.agency/` for persistent memory across sessions.

## Skill Execution Order

| # | Skill | Folder | Purpose | Output File |
|---|---|---|---|---|
| 01 | Client Discovery | `uiux-client-discovery/` | Collect project, business, audience, brand, and technical details | `.agency/CLIENT_BRIEF.md` |
| 02 | UX Strategy | `uiux-strategy-skill/` | Convert brief into UX strategy, user journey, page hierarchy, conversion flow | `.agency/UX_STRATEGY.md` |
| 03 | Design DNA | `uiux-desig-dna/` | Define visual direction, color system, typography, layout, anti-AI rules | `.agency/DESIGN_DNA.md` |
| 04 | Stitch Prompt | `uiux-stitch-prompt/` | Generate ready-to-paste Google Stitch prompt | `.agency/STITCH_PROMPT.md` |
| 05 | UI Critique | `uiux-critic-skill/` | Review generated UI against brief, UX strategy, and Design DNA | `.agency/UI_CRITIQUE.md` |
| 06 | Humanization | `uiux-humanization-skill/` | Convert critique into refinement plan and Stitch refinement prompt | `.agency/REFINEMENT_PROMPT.md` |
| 07 | Responsive Review | `uiux-responsive-access/` | Check responsive behavior and accessibility before handoff | `.agency/RESPONSIVE_ACCESSIBILITY_REVIEW.md` |
| 08 | Developer Handoff | `uiux-developer-handoff/` | Convert approved design into implementation-ready documentation | `.agency/DEVELOPER_HANDOFF.md` |
| 09 | Project Memory | `project-memory-continuity-skill/` | Initialize, maintain, repair, and resume project memory | `.agency/` files |

---

## How To Use The Skills

### In Claude Code (CLI or Desktop)

Each skill is invoked using a `/` command. Type the skill name as a slash command in Claude Code:

| Skill | Command |
|---|---|
| Client Discovery | `/uiux-client-discovery` |
| UX Strategy | `/uiux-strategy-skill` |
| Design DNA | `/uiux-desig-dna` |
| Stitch Prompt Generator | `/uiux-stitch-prompt` |
| UI Critique | `/uiux-critic-skill` |
| Humanization & Refinement | `/uiux-humanization-skill` |
| Responsive + Accessibility Review | `/uiux-responsive-access` |
| Developer Handoff | `/uiux-developer-handoff` |
| Project Memory & Continuity | `/project-memory-continuity-skill` |

### Step-By-Step Workflow

**Step 1 — Start a new project**

```
/uiux-client-discovery
```

Claude will ask discovery questions and produce a Project UI Brief. It also creates the `.agency/` folder in your project.

---

**Step 2 — Create UX Strategy**

```
/uiux-strategy-skill
```

Requires the Project UI Brief from Step 1. Claude reads `.agency/CLIENT_BRIEF.md` and produces a UX Strategy Document.

---

**Step 3 — Create Design DNA**

```
/uiux-desig-dna
```

Requires brief + UX strategy. Claude defines visual direction, colors, typography, layout rules, and anti-AI design rules.

---

**Step 4 — Generate Stitch Prompt**

```
/uiux-stitch-prompt
```

Requires brief + UX strategy + Design DNA. Claude produces a ready-to-paste Google Stitch prompt.

Paste the output into [Google Stitch](https://stitch.withgoogle.com) to generate the UI concept.

---

**Step 5 — Critique The Generated UI**

After generating a UI in Google Stitch, bring the result back:

```
/uiux-critic-skill

[paste screenshot or describe the generated UI]
```

Claude scores the UI and produces a structured critique report.

---

**Step 6 — Humanize And Refine**

```
/uiux-humanization-skill
```

Reads the critique. Produces a humanization plan and a Google Stitch refinement prompt. Paste the refinement prompt back into Stitch.

---

**Step 7 — Responsive + Accessibility Review**

```
/uiux-responsive-access
```

Reviews the final UI concept for mobile behavior, touch targets, contrast, and accessibility basics.

---

**Step 8 — Developer Handoff**

```
/uiux-developer-handoff
```

Converts the approved design into a full developer handoff document with design tokens, component inventory, responsive rules, states, and implementation notes.

---

**Step 9 — Resume or Repair Context (any time)**

```
/project-memory-continuity-skill
```

Use this at the start of any new session to restore project context without re-running previous skills.

---

### Quick Trigger Phrases

You can also trigger each skill by describing what you want:

| What you say | Skill triggered |
|---|---|
| "Start a new client UI project" | Client Discovery |
| "Run UX strategy for this brief" | UX Strategy |
| "Create the Design DNA" | Design DNA |
| "Generate the Stitch prompt" | Stitch Prompt |
| "Review this UI" / "Critique this screenshot" | UI Critique |
| "Humanize this UI" / "Make it less AI-generated" | Humanization |
| "Check mobile readiness" / "Review before handoff" | Responsive Review |
| "Create developer handoff" | Developer Handoff |
| "Resume this project" / "What is the current state?" | Project Memory |

---

## How `.agency/` Memory Works

Every client project has an `.agency/` folder in its root directory.

This folder is the persistent memory for the project. It enables any AI tool to resume work without previous chat history.

### Context Loading Rule

Every skill follows this rule:

1. Read `.agency/CURRENT_CONTEXT.md` first — lightweight snapshot
2. Read `.agency/CONTEXT_INDEX.json` second — tells AI what to read next
3. Read only the required files for the active skill
4. Do not read all `.md` files by default

### Why CURRENT_CONTEXT.md Is Read First

It contains the project snapshot, current phase, completed work, current task, and what must not be changed. Reading it first gives the AI everything it needs to continue without restarting.

### Why CONTEXT_INDEX.json Prevents Reading All Files

It contains `required_context_files` for each skill phase. The AI only reads those specific files — not every markdown file in the project.

---

## How To Start A New Client Project

1. Create a new project folder.
2. Copy `agency-memory-template/` into the project root as `.agency/`.
3. Run the Client Discovery Skill.
4. Follow the skill execution order.

---

## How To Resume A Project In A New Session

Paste this into any AI tool at the start of a session:

```
Resume this project from repo memory.

Do not use previous chat history.
Do not start from zero.
Do not scan all markdown files.

First read:
1. .agency/CURRENT_CONTEXT.md
2. .agency/CONTEXT_INDEX.json

Then read only the files listed in CONTEXT_INDEX.json for the current task.

After reading, summarize:
- What this project is
- Current phase
- Completed work
- In-progress work
- Pending work
- Current task
- Design rules to follow
- Files likely relevant
- Things not to change

Then continue with the current task only.
```

---

## How To Update Project Memory After Each Task

Every skill automatically updates memory after completing work:

1. Saves skill output to its mapped `.agency` file
2. Updates `.agency/CURRENT_CONTEXT.md`
3. Updates `.agency/PROJECT_STATE.json`
4. Updates `.agency/CONTEXT_INDEX.json`
5. Appends entry to `.agency/CHANGELOG.md`
6. Updates `.agency/TODO.md`
7. Adds major decisions to `.agency/DECISIONS.md`

---

## File Structure

```txt
uiux/
├── README.md                           ← This file
├── agency-memory-template/             ← Copy this into client projects as .agency/
│   ├── README.md
│   ├── AI_INSTRUCTIONS.md
│   ├── CURRENT_CONTEXT.md
│   ├── CONTEXT_INDEX.json
│   ├── PROJECT_CONTEXT.md
│   ├── PROJECT_STATE.json
│   ├── CLIENT_BRIEF.md
│   ├── UX_STRATEGY.md
│   ├── DESIGN_DNA.md
│   ├── STITCH_PROMPT.md
│   ├── UI_CRITIQUE.md
│   ├── REFINEMENT_PROMPT.md
│   ├── RESPONSIVE_ACCESSIBILITY_REVIEW.md
│   ├── DEVELOPER_HANDOFF.md
│   ├── DECISIONS.md
│   ├── TODO.md
│   └── CHANGELOG.md
├── uiux-client-discovery/
│   └── SKILL.md
├── uiux-strategy-skill/
│   └── SKILL.md
├── uiux-desig-dna/
│   └── SKILL.md
├── uiux-stitch-prompt/
│   └── SKILL.md
├── uiux-critic-skill/
│   └── SKILL.md
├── uiux-humanization-skill/
│   └── SKILL.md
├── uiux-responsive-access/
│   └── SKILL.md
├── uiux-developer-handoff/
│   └── SKILL.md
└── project-memory-continuity-skill/
    └── SKILL.md
```

---

## Skill Memory Behavior Summary

Each skill follows this pattern:

**Before running:**
1. Check `.agency/` exists
2. Read `CURRENT_CONTEXT.md`
3. Read `CONTEXT_INDEX.json`
4. Read only required files for this skill

**After completing:**
1. Save output to mapped `.agency` file
2. Update `CURRENT_CONTEXT.md`
3. Update `PROJECT_STATE.json`
4. Update `CONTEXT_INDEX.json`
5. Append to `CHANGELOG.md`
6. Update `TODO.md`
7. Add decisions to `DECISIONS.md`
