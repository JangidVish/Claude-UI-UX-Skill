# UI/UX Agency Skill System

A complete AI-assisted UI/UX workflow for web agencies. Each skill handles one phase of the project and saves its output to `.agency/` for persistent memory across sessions.

## Skill Execution Order

| # | Skill | Folder | Purpose | Output File |
|---|---|---|---|---|
| 00 | Competitive Analysis | `uiux-competitive-analysis/` | Browser automation — screenshot and analyze 3–5 competitor sites | `.agency/COMPETITIVE_ANALYSIS.md` |
| 01 | Client Discovery | `uiux-client-discovery/` | Collect project brief, set project_complexity and generation_tool | `.agency/CLIENT_BRIEF.md` |
| 01.5 | Persona & JTBD | `uiux-persona-jtbd/` | Build proto-personas and Jobs-To-Be-Done from brief — informs UX, design, and copy | `.agency/PERSONAS.md` |
| 02 | UX Strategy | `uiux-strategy-skill/` | Convert brief into UX strategy, user journey, page hierarchy, conversion flow | `.agency/UX_STRATEGY.md` |
| 02.5 | Wireframe & IA | `uiux-wireframe-ia/` | Text wireframes to validate structure before visual design — human checkpoint | `.agency/WIREFRAMES.md` |
| 03 | Design DNA | `uiux-desig-dna/` | Define visual direction, color system, typography, layout, anti-AI rules | `.agency/DESIGN_DNA.md` |
| 03.5 | Design Direction | `uiux-design-direction/` | Generate 3 visual directions, human picks one — human checkpoint | `.agency/DESIGN_DIRECTION_OPTIONS.md` |
| 04 | UI Generation Prompt | `uiux-stitch-prompt/` | Generate tool-agnostic UI prompt (Stitch, V0, Framer, Figma, Locofy) | `.agency/UI_GENERATION_PROMPT.md` |
| 05 | UI Critique | `uiux-critic-skill/` | Review generated UI with screenshot — human checkpoint | `.agency/UI_CRITIQUE.md` |
| 06 | Humanization | `uiux-humanization-skill/` | Remove AI smell, produce refinement prompt | `.agency/REFINEMENT_PROMPT.md` |
| 06.5 | Content Strategy | `uiux-content-strategy/` | Write real copy — headlines, CTAs, microcopy, SEO copy for every page | `.agency/CONTENT_STRATEGY.md` |
| 07 | Responsive Review | `uiux-responsive-access/` | Check responsive behavior and accessibility before handoff | `.agency/RESPONSIVE_ACCESSIBILITY_REVIEW.md` |
| 08 | Developer Handoff | `uiux-developer-handoff/` | Convert approved design into implementation-ready documentation | `.agency/DEVELOPER_HANDOFF.md` |
| 08.5 | Design System Export | `uiux-design-system-export/` | Generate CSS custom properties, design tokens JSON, and Tailwind config | `.agency/DESIGN_SYSTEM.css` + `.agency/DESIGN_SYSTEM_TOKENS.json` |
| 09 | Project Memory | `project-memory-continuity-skill/` | Initialize, maintain, repair, and resume project memory | `.agency/` files |
| 10 | Client Presentation | `uiux-client-presentation/` | Assemble all project work into a client-facing presentation document | `.agency/CLIENT_PRESENTATION.md` |

---

## How To Use The Skills

### In Claude Code (CLI or Desktop)

Each skill is invoked using a `/` command. Type the skill name as a slash command in Claude Code:

| Skill | Command |
|---|---|
| Competitive Analysis | `/uiux-competitive-analysis` |
| Client Discovery | `/uiux-client-discovery` |
| Persona & JTBD | `/uiux-persona-jtbd` |
| UX Strategy | `/uiux-strategy-skill` |
| Wireframe & IA | `/uiux-wireframe-ia` |
| Design DNA | `/uiux-desig-dna` |
| Design Direction | `/uiux-design-direction` |
| UI Generation Prompt | `/uiux-stitch-prompt` |
| UI Critique | `/uiux-critic-skill` |
| Humanization & Refinement | `/uiux-humanization-skill` |
| Content Strategy | `/uiux-content-strategy` |
| Responsive + Accessibility Review | `/uiux-responsive-access` |
| Developer Handoff | `/uiux-developer-handoff` |
| Design System Export | `/uiux-design-system-export` |
| Client Presentation | `/uiux-client-presentation` |
| Project Memory & Continuity | `/project-memory-continuity-skill` |

### Step-By-Step Workflow

**Step 0 — Competitive Analysis (standard and full projects)**

```
/uiux-competitive-analysis
```

Provide 2–5 competitor URLs from the brief. Claude uses browser automation to screenshot and analyze each site. Produces a differentiation strategy that feeds into Design DNA.

Skip for lite projects.

---

**Step 1 — Start a new project**

```
/uiux-client-discovery
```

Claude will ask discovery questions and produce a Project UI Brief. It also creates the `.agency/` folder in your project.

---

**Step 1.5 — Persona & JTBD (standard and full projects)**

```
/uiux-persona-jtbd
```

Reads the Client Brief. Builds proto-personas (behavior models, not stock-photo stereotypes), Jobs-To-Be-Done statements, friction audits, and design implications per persona. Feeds into UX Strategy, Design DNA, and Content Strategy. Run before UX Strategy for clearer, more targeted decisions.

Skip for lite projects.

---

**Step 2 — Create UX Strategy**

```
/uiux-strategy-skill
```

Requires the Project UI Brief from Step 1. Claude reads `.agency/CLIENT_BRIEF.md` and produces a UX Strategy Document.

---

**Step 2.5 — Wireframe & IA Validation (standard and full projects)**

```
/uiux-wireframe-ia
```

Claude converts UX Strategy into text-based ASCII wireframes for each page. Validates section order, content priority, and mobile stacking before visual design begins. **Requires human approval before proceeding.**

---

**Step 3 — Create Design DNA**

```
/uiux-desig-dna
```

Requires brief + UX strategy. Claude defines visual direction, colors, typography, layout rules, and anti-AI design rules.

---

**Step 3.5 — Design Direction Selector (standard and full projects)**

```
/uiux-design-direction
```

Claude generates three named visual directions with distinct personalities. Human or client picks one. Chosen direction feeds into Design DNA. **Requires human selection before proceeding.**

---

**Step 4 — Generate UI Prompt**

```
/uiux-stitch-prompt
```

Requires brief + UX strategy + Design DNA. Claude reads `generation_tool` from `PROJECT_STATE.json` and produces a tool-specific prompt optimized for whichever tool was chosen during discovery (Google Stitch, V0, Framer AI, Figma, or Locofy). Paste the output into the chosen tool to generate the UI concept.

---

**Step 5 — Critique The Generated UI**

After generating a UI in your chosen tool, bring the result back:

```
/uiux-critic-skill

[paste screenshot or URL]
```

Provide a screenshot or URL — the skill requires visual input before running. Claude scores the UI across 6 categories and produces a structured critique report with a must-fix list.

---

**Step 6 — Humanize And Refine**

```
/uiux-humanization-skill
```

Reads the critique. Produces a humanization plan (what specifically makes it look AI-generated) and a refinement prompt to paste back into your generation tool.

---

**Step 6.5 — Content Strategy (standard and full projects)**

```
/uiux-content-strategy
```

Reads brief + UX strategy + Design DNA. Generates real copy for every page section: headlines, subheadlines, body copy, CTAs, microcopy, form labels, and SEO meta tags. Run before UI generation so prompts use real copy — or before handoff to give developers final content.

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

**Step 8.5 — Design System Export (standard and full projects)**

```
/uiux-design-system-export
```

Reads Design DNA + Developer Handoff. Generates three production-ready files: CSS custom properties (`:root` variables), W3C design token JSON (importable into Figma and Style Dictionary), and a Tailwind config extension block. Developers paste these directly into the project.

---

**Step 9 — Resume or Repair Context (any time)**

```
/project-memory-continuity-skill
```

Use this at the start of any new session to restore project context without re-running previous skills.

---

**Step 10 — Client Presentation (standard and full projects)**

```
/uiux-client-presentation
```

Assembles all completed project work into a client-facing presentation document. Translates design decisions into language the client understands. Use before design review calls or when handing off to the client's team.

---

### Quick Trigger Phrases

You can also trigger each skill by describing what you want:

| What you say | Skill triggered |
|---|---|
| "Analyze competitors" / "Screenshot these competitor sites" | Competitive Analysis |
| "Start a new client UI project" | Client Discovery |
| "Build personas" / "Who are the users?" / "Create JTBD" | Persona & JTBD |
| "Run UX strategy for this brief" | UX Strategy |
| "Create wireframes" / "Validate the IA" | Wireframe & IA |
| "Create the Design DNA" | Design DNA |
| "Show me design direction options" / "Give me 3 design directions" | Design Direction |
| "Generate the UI prompt" / "Generate the Stitch prompt" | UI Generation Prompt |
| "Review this UI" / "Critique this screenshot" | UI Critique |
| "Humanize this UI" / "Make it less AI-generated" | Humanization |
| "Write the copy" / "Generate content strategy" / "Write headlines" | Content Strategy |
| "Check mobile readiness" / "Review before handoff" | Responsive Review |
| "Create developer handoff" | Developer Handoff |
| "Export design tokens" / "Generate CSS variables" | Design System Export |
| "Create client presentation" / "Prepare for client review" | Client Presentation |
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

## Project Complexity Guide

Set during Client Discovery (Step 1). Controls which skills run.

| Complexity | When | Skills That Run |
|---|---|---|
| **Lite** | Single landing page, 1–2 day turnaround | 01, 02, 03, 04, 05, 06, 07, 08 |
| **Standard** | Multi-page website or web app, 1–2 weeks | All skills |
| **Full** | Complex product with multiple user flows, 2+ weeks | All skills + extended research |

**Lite projects skip:** Competitive Analysis (00), Persona & JTBD (01.5), Wireframe & IA (02.5), Design Direction (03.5), Content Strategy (06.5), Design System Export (08.5), Client Presentation (10)

**Human checkpoints** (skills that wait for your input before continuing):

| Skill | What It Waits For |
|---|---|
| Wireframe & IA (02.5) | You approve the wireframe structure |
| Design Direction (03.5) | You pick one of three visual directions |
| UI Critique (05) | You provide a screenshot or URL of the generated UI |

---

## How To Start A New Client Project

1. Create a new project folder.
2. Copy `agency-memory-template/` into the project root as `.agency/`.
3. Open Claude Code in that folder.
4. Run `/uiux-client-discovery` and answer the discovery questions.
5. Follow the skill execution order from there.

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
│   ├── COMPETITIVE_ANALYSIS.md
│   ├── PERSONAS.md
│   ├── UX_STRATEGY.md
│   ├── WIREFRAMES.md
│   ├── DESIGN_DNA.md
│   ├── DESIGN_DIRECTION_OPTIONS.md
│   ├── UI_GENERATION_PROMPT.md
│   ├── CONTENT_STRATEGY.md
│   ├── UI_CRITIQUE.md
│   ├── REFINEMENT_PROMPT.md
│   ├── RESPONSIVE_ACCESSIBILITY_REVIEW.md
│   ├── DEVELOPER_HANDOFF.md
│   ├── DESIGN_SYSTEM.css
│   ├── DESIGN_SYSTEM_TOKENS.json
│   ├── CLIENT_PRESENTATION.md
│   ├── DECISIONS.md
│   ├── TODO.md
│   └── CHANGELOG.md
├── uiux-competitive-analysis/
│   └── SKILL.md
├── uiux-client-discovery/
│   └── SKILL.md
├── uiux-persona-jtbd/
│   └── SKILL.md
├── uiux-strategy-skill/
│   └── SKILL.md
├── uiux-wireframe-ia/
│   └── SKILL.md
├── uiux-desig-dna/
│   └── SKILL.md
├── uiux-design-direction/
│   └── SKILL.md
├── uiux-stitch-prompt/
│   └── SKILL.md
├── uiux-critic-skill/
│   └── SKILL.md
├── uiux-humanization-skill/
│   └── SKILL.md
├── uiux-content-strategy/
│   └── SKILL.md
├── uiux-responsive-access/
│   └── SKILL.md
├── uiux-developer-handoff/
│   └── SKILL.md
├── uiux-design-system-export/
│   └── SKILL.md
├── uiux-client-presentation/
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
