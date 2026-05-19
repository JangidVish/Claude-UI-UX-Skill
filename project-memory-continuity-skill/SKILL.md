# Project Memory & Continuity Skill

**Skill Number:** 09

## Purpose

This skill creates, maintains, repairs, and uses the `.agency/` project memory system.

It ensures that any AI tool — Claude CLI, Claude Code, Codex, ChatGPT, Cursor, or a developer — can resume work on a project without needing previous chat history.

## When To Use

Use this skill:

- At the start of a new client project (before Client Discovery Skill)
- When entering a new Claude or Codex or ChatGPT session on an existing project
- When project context is lost or the AI session has no history
- Before continuing development after a gap
- After a major design or code change
- Before developer handoff
- When `.agency/` files are missing or outdated
- When the AI is starting from zero and needs to reconstruct context

## Core Behavior

1. Check if `.agency/` exists.
2. If missing, create it from the standard template structure.
3. If present, read `CURRENT_CONTEXT.md` first.
4. Read `CONTEXT_INDEX.json` second.
5. Load only the files listed under `required_context_files`.
6. Summarize the current project state clearly.
7. Update stale files if needed.
8. Preserve all decisions and changelog entries.
9. Prepare next-task context for the active skill or development task.

## Context Loading Rule

Never read all project markdown files by default.

Always load context in this order:

1. `.agency/CURRENT_CONTEXT.md` — lightweight, always first
2. `.agency/CONTEXT_INDEX.json` — tells AI what to read next
3. Required files only — based on `required_context_files` in the index
4. Source code only if the task requires coding

---

## `.agency/` Folder Structure

The `.agency/` folder should exist in the client project root:

```txt
.agency/
├── README.md
├── AI_INSTRUCTIONS.md
├── CURRENT_CONTEXT.md
├── CONTEXT_INDEX.json
├── PROJECT_CONTEXT.md
├── PROJECT_STATE.json
├── CLIENT_BRIEF.md
├── UX_STRATEGY.md
├── DESIGN_DNA.md
├── STITCH_PROMPT.md
├── UI_CRITIQUE.md
├── REFINEMENT_PROMPT.md
├── RESPONSIVE_ACCESSIBILITY_REVIEW.md
├── DEVELOPER_HANDOFF.md
├── DECISIONS.md
├── TODO.md
└── CHANGELOG.md
```

---

## CURRENT_CONTEXT.md Template

When creating or updating `.agency/CURRENT_CONTEXT.md`, use this structure:

```md
# Current Context

## Project Snapshot

Client/Product:
Project Type:
Industry:
Current Phase:
Primary Goal:
Primary CTA:
Target Audience:
Design Direction:

## Current State

Completed:
-

In Progress:
-

Pending:
-

Blocked:
-

## Current Task

Task:

## Active Skill

Skill Name:
Skill Purpose:

## Files Relevant For Current Task

-

## Do Not Do

- Do not restart the project from zero.
- Do not redesign completed work unless explicitly requested.
- Do not change design direction unless requested.
- Do not overwrite existing `.agency` files without preserving history.

## Next Recommended Step

Next Step:
```

---

## CONTEXT_INDEX.json Template

When creating or updating `.agency/CONTEXT_INDEX.json`, use this structure:

```json
{
  "version": "1.0",
  "project_name": "",
  "current_phase": "",
  "current_skill": "",
  "last_updated": "",
  "context_loading_rule": "Read CURRENT_CONTEXT.md first. Read only the files listed in required_context_files for the active skill.",
  "active_task": "",
  "required_context_files": [],
  "files": {
    "project_context": {
      "path": ".agency/PROJECT_CONTEXT.md",
      "purpose": "Full project summary, client input, goals, audience, assumptions, and design risks",
      "read_when": ["client discovery", "major project reorientation", "handoff"]
    },
    "project_state": {
      "path": ".agency/PROJECT_STATE.json",
      "purpose": "Machine-readable current project state",
      "read_when": ["every skill if state details are needed"]
    },
    "client_brief": {
      "path": ".agency/CLIENT_BRIEF.md",
      "purpose": "Output from Client Discovery Skill",
      "read_when": ["ux strategy", "design dna", "stitch prompt", "handoff"]
    },
    "ux_strategy": {
      "path": ".agency/UX_STRATEGY.md",
      "purpose": "UX strategy, journey, page hierarchy, conversion flow",
      "read_when": ["design dna", "stitch prompt", "critique", "handoff"]
    },
    "design_dna": {
      "path": ".agency/DESIGN_DNA.md",
      "purpose": "Visual design system, colors, typography, layout, motion, anti-AI rules",
      "read_when": ["stitch prompt", "critique", "humanization", "responsive review", "handoff"]
    },
    "stitch_prompt": {
      "path": ".agency/STITCH_PROMPT.md",
      "purpose": "Final Google Stitch prompt",
      "read_when": ["critique", "humanization"]
    },
    "ui_critique": {
      "path": ".agency/UI_CRITIQUE.md",
      "purpose": "Critique of generated UI output",
      "read_when": ["humanization", "handoff if needed"]
    },
    "refinement_prompt": {
      "path": ".agency/REFINEMENT_PROMPT.md",
      "purpose": "Prompt used to improve generated UI",
      "read_when": ["critique", "handoff if needed"]
    },
    "responsive_accessibility_review": {
      "path": ".agency/RESPONSIVE_ACCESSIBILITY_REVIEW.md",
      "purpose": "Responsive and accessibility review",
      "read_when": ["developer handoff"]
    },
    "developer_handoff": {
      "path": ".agency/DEVELOPER_HANDOFF.md",
      "purpose": "Final implementation handoff",
      "read_when": ["development"]
    },
    "decisions": {
      "path": ".agency/DECISIONS.md",
      "purpose": "Important project decisions that should not be forgotten",
      "read_when": ["before changing design direction", "before major implementation"]
    },
    "todo": {
      "path": ".agency/TODO.md",
      "purpose": "Current and upcoming tasks",
      "read_when": ["every new session", "before continuing work"]
    },
    "changelog": {
      "path": ".agency/CHANGELOG.md",
      "purpose": "History of completed work",
      "read_when": ["when resuming after a gap", "handoff"]
    }
  }
}
```

---

## PROJECT_STATE.json Template

When creating or updating `.agency/PROJECT_STATE.json`, use this structure:

```json
{
  "project_name": "",
  "client": "",
  "industry": "",
  "project_type": "",
  "current_phase": "",
  "last_updated": "",
  "phases": {
    "discovery": { "status": "pending", "completed_at": null },
    "ux_strategy": { "status": "pending", "completed_at": null },
    "design_dna": { "status": "pending", "completed_at": null },
    "stitch_prompt": { "status": "pending", "completed_at": null },
    "ui_critique": { "status": "pending", "completed_at": null },
    "humanization": { "status": "pending", "completed_at": null },
    "responsive_review": { "status": "pending", "completed_at": null },
    "developer_handoff": { "status": "pending", "completed_at": null }
  },
  "handoff_complete": false,
  "primary_cta": "",
  "design_direction": "",
  "target_audience": "",
  "open_questions": [],
  "blocked_by": []
}
```

---

## Resume Process

When resuming any project in a new session:

### Step 1

Read `.agency/CURRENT_CONTEXT.md` immediately. Do not read anything else first.

### Step 2

Read `.agency/CONTEXT_INDEX.json`. Check `required_context_files` and `current_skill`.

### Step 3

Read only the files listed in `required_context_files`.

### Step 4

Summarize:

1. What this project is
2. Current phase
3. Completed work
4. In-progress work
5. Pending work
6. Current task
7. Design rules to follow
8. Files likely relevant
9. Things not to change

### Step 5

Continue with the current task. Do not restart from zero.

---

## Repair Process

If `.agency/` files are missing, incomplete, or stale:

1. Check which files exist using the folder structure above.
2. For missing files, create empty templates.
3. For stale `CURRENT_CONTEXT.md`, update it from available `.agency/` files.
4. For stale `CONTEXT_INDEX.json`, rebuild it from available files.
5. Preserve all existing content — never delete decisions or changelog entries.
6. Set `last_updated` in `CONTEXT_INDEX.json` to today's date.

---

## Skill Output Files

This skill updates:

- `.agency/CURRENT_CONTEXT.md`
- `.agency/CONTEXT_INDEX.json`
- `.agency/PROJECT_STATE.json`
- `.agency/TODO.md`
- `.agency/CHANGELOG.md`
- Any missing `.agency/` files

---

## Example Trigger Phrases

Use this skill when the user says:

- "Resume this project."
- "What is the current project state?"
- "Initialize project memory."
- "Create the .agency folder."
- "Update project context."
- "Repair missing agency files."
- "Start fresh session for this project."
- "What did we complete last time?"
- "Prepare context for a new Claude session."
- "Update the context index."

---

## The Universal Resume Prompt

Use this prompt in any new Claude CLI, Claude Code, Codex, ChatGPT, or Cursor session:

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

## Project Memory Behavior

This skill itself uses `.agency/` memory:

1. Always read `.agency/CURRENT_CONTEXT.md` first.
2. Always read `.agency/CONTEXT_INDEX.json` second.
3. Only load deeper files if needed.
4. After completing memory initialization or repair, update all relevant `.agency/` files.
5. Do not delete any existing content.
