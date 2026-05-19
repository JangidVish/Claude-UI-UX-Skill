# .agency/ Project Memory System

This folder is the persistent memory system for AI-assisted UI/UX projects.

It enables any AI tool — Claude CLI, Claude Code, Codex, ChatGPT, Cursor, or a developer — to resume work without needing previous chat history.

## How It Works

Every client project should have an `.agency/` folder in its root directory.

When an AI tool or developer starts a new session, they read:

1. `CURRENT_CONTEXT.md` first — lightweight project snapshot
2. `CONTEXT_INDEX.json` second — tells the AI what files to read next
3. Only the required files for the current task

This prevents the AI from reading all markdown files repeatedly and losing context.

## File Purposes

| File | Purpose |
|---|---|
| `CURRENT_CONTEXT.md` | Lightweight session file. Read first every time. |
| `CONTEXT_INDEX.json` | Machine-readable file map. Read second. Controls what to load. |
| `PROJECT_CONTEXT.md` | Full project summary, goals, audience, assumptions. |
| `PROJECT_STATE.json` | Machine-readable phase tracking and project state. |
| `CLIENT_BRIEF.md` | Output from Client Discovery Skill. |
| `UX_STRATEGY.md` | UX strategy, journey, page hierarchy, conversion flow. |
| `DESIGN_DNA.md` | Visual design system, colors, typography, motion, anti-AI rules. |
| `STITCH_PROMPT.md` | Final Google Stitch prompt. |
| `UI_CRITIQUE.md` | Critique of generated UI output. |
| `REFINEMENT_PROMPT.md` | Prompt used to improve generated UI. |
| `RESPONSIVE_ACCESSIBILITY_REVIEW.md` | Responsive and accessibility review. |
| `DEVELOPER_HANDOFF.md` | Final implementation handoff. |
| `DECISIONS.md` | Important project decisions that should not be forgotten. |
| `TODO.md` | Current and upcoming tasks. |
| `CHANGELOG.md` | History of completed work. |
| `AI_INSTRUCTIONS.md` | AI behavior rules for this project. |

## How To Use In A New Session

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
- Things not to change

Then continue with the current task only.
```

## How To Set Up For A New Project

Copy this entire folder into the client project root and rename it `.agency/`.

Then run the Client Discovery Skill to populate the files.
