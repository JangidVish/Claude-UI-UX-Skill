# AI Instructions For This Project

## Context Loading Rule

Never read all project markdown files by default.

Always load context in this order:

1. `.agency/CURRENT_CONTEXT.md` — read this first, every session
2. `.agency/CONTEXT_INDEX.json` — read this second, check required files
3. Required files only — based on `required_context_files` in the index
4. Source code only if the task requires coding

## Do Not Do

- Do not restart the project from zero.
- Do not redesign completed work unless explicitly requested.
- Do not change design direction unless requested.
- Do not overwrite existing `.agency` files without preserving history.
- Do not ask for information already present in `.agency/` files.
- Do not read all `.md` files by default.
- Do not delete decisions or changelog entries.

## After Completing Any Task

1. Update `.agency/CURRENT_CONTEXT.md`.
2. Update `.agency/PROJECT_STATE.json`.
3. Update `.agency/CONTEXT_INDEX.json`.
4. Append a short entry to `.agency/CHANGELOG.md`.
5. Update `.agency/TODO.md`.
6. Add major decisions to `.agency/DECISIONS.md`.
7. Write skill output to its mapped file.

## Session Resume Protocol

When a new session starts with no chat history:

1. Read `.agency/CURRENT_CONTEXT.md`.
2. Read `.agency/CONTEXT_INDEX.json`.
3. Read only required files.
4. Summarize project state.
5. Continue from current task.
6. Do not ask the user to repeat context.
