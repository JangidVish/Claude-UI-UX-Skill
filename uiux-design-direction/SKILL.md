---
skill_id: uiux-design-direction
skill_number: 03.5
requires_visual_input: false
requires_browser: false
project_complexity: standard, full
human_checkpoint_after: true
output_file: .agency/DESIGN_DIRECTION_OPTIONS.md
runs_between: uiux-desig-dna, uiux-stitch-prompt
---

# Design Direction Selector Skill

## Purpose

This skill generates three distinct visual design directions before the Design DNA is finalized.

The goal is to prevent the team from committing to one visual direction without considering alternatives — a common cause of client revision cycles and AI-generic output.

Each direction is a named creative concept with a distinct personality, color approach, typography direction, layout philosophy, and differentiation angle.

A human or client chooses one direction. The chosen direction becomes the foundation for the Design DNA Document.

The output is a **Design Direction Options Document** with three named directions ready for selection.

---

## When To Use

Use this skill after:

1. Client Discovery Skill
2. UX Strategy Skill
3. Wireframe & IA Validation Skill (if run)
4. Competitive Analysis Skill (if run — strongly recommended input)

Use it before:

- Design DNA Skill

Do not use this skill after Design DNA is already locked. If the direction is already approved, proceed directly to the UI Generation Prompt Skill.

---

## Core Behavior

When this skill is triggered, act as a senior creative director and visual design strategist.

Your job is to:

1. Read the Project UI Brief.
2. Read the UX Strategy Document.
3. Read the Competitive Analysis Report if available.
4. Identify what the market currently looks like.
5. Identify what visual territory is unoccupied.
6. Generate three meaningfully different design directions.
7. Name each direction clearly.
8. Describe each direction in a way a client or designer can evaluate without seeing a mockup.
9. Present all three for human selection.
10. After selection, confirm the chosen direction and prepare it for Design DNA input.

---

## Important Rules

### 1. Three Directions Must Be Meaningfully Different

Do not generate three variations of the same idea.

Bad — three variations of the same direction:
```
Direction A: Modern and clean
Direction B: Modern and minimal
Direction C: Clean and contemporary
```

Good — three genuinely different territories:
```
Direction A: Quiet Luxury Editorial
Direction B: Bold Technical Intelligence
Direction C: Warm Human Consultancy
```

Each direction should feel like a different brand could own it.

### 2. No Colors or Fonts Yet — Direction Only

Do not define specific hex codes or font names in this skill.

Define direction in terms of:
- Color territory (warm neutrals, deep navy, high contrast monochrome)
- Typography personality (editorial serif, technical grotesk, humanist sans)
- Layout philosophy (spacious image-led, dense data-rich, generous whitespace)
- Motion personality (slow and refined, fast and precise, gentle and warm)

Specific values are defined in the Design DNA Skill after a direction is chosen.

### 3. Tie Each Direction To Business Goals

Each direction must explain how it supports the conversion goal and target audience — not just how it looks.

Example:
```
Direction A: Quiet Luxury Editorial
Why it works for this project: Premium homeowners expect restraint and quality. This direction signals taste and credibility before a word is read.
```

### 4. Reference Comparable Brands, Not Competitors

Reference brands outside the client's industry to illustrate the feel.

Good:
```
Comparable feel: Aesop, Kinfolk magazine, Bottega Veneta website
```

Not:
```
Comparable to: [direct competitor name]
```

### 5. Always End With A Human Checkpoint

After presenting all three directions, always ask:

```
Which direction resonates most for this project?

Reply with A, B, or C — or describe what you like from multiple directions and I will create a hybrid.

You can also request a fourth direction if none of these feel right.
```

Do not proceed to Design DNA until a direction is chosen.

---

## Direction Generation Process

### Step 1: Read Brief And Strategy

Extract:
- Industry and market positioning
- Target audience emotional expectations
- Business goal and CTA
- Brand personality words (to describe AND avoid)
- Visual tone preference if given

### Step 2: Read Competitive Analysis (If Available)

Extract:
- Common visual patterns in the market
- Visual fatigue patterns to avoid
- Unoccupied visual territory
- What competitors do poorly

### Step 3: Identify Three Different Creative Territories

Think across these axes:

**Axis 1: Emotional register**
Restrained ↔ Expressive
Warm ↔ Cool
Serious ↔ Playful

**Axis 2: Visual density**
Spacious editorial ↔ Dense information-rich

**Axis 3: Design language era/style**
Classic refined ↔ Modern technical ↔ Contemporary warm

Place each direction at a genuinely different position across these axes.

### Step 4: Name Each Direction

Give each direction:
- A short evocative name (2–4 words)
- A one-sentence personality statement

Examples:
- Quiet Luxury Editorial: "Spacious, image-led confidence that lets the work speak."
- Sharp Technical Intelligence: "Dense, precise, data-literate — built for the analytical mind."
- Warm Expert Companion: "Approachable, human, and trustworthy without sacrificing credibility."

### Step 5: Write Each Direction Profile

Use the Direction Profile Format below.

### Step 6: Present For Selection

Present all three. Ask for a choice.

### Step 7: Confirm Chosen Direction

After selection, output a **Chosen Direction Summary** that the Design DNA Skill will use as its starting point.

---

## Direction Profile Format

For each direction:

```md
## Direction [A/B/C]: [Name]

**One-Line Personality:**
[One sentence that defines the feel]

**Mood Keywords:**
[5 words that describe the visual feel]

**Color Territory:**
[Color description — no hex codes. Examples: warm ivory and charcoal, deep navy and cream, high-contrast black and white with one bold accent]

**Typography Personality:**
[Font category direction. Examples: editorial serif + clean sans, technical grotesk, humanist sans, luxury display + neutral body]

**Layout Philosophy:**
[Describe the layout approach. Examples: spacious and image-led, structured and data-dense, editorial variety with breathing room]

**Motion Personality:**
[Describe motion. Examples: slow and elegant, fast and precise, gentle and minimal]

**Comparable Brands:**
[2–3 brand references outside the client's direct industry]

**Why This Works For This Project:**
[One paragraph connecting this direction to the business goal and target audience]

**What Makes It Distinctive:**
[How this differs from what competitors currently do]

**What This Direction Avoids:**
[2–3 design patterns this direction explicitly rejects]
```

---

## Output Format

```md
# Design Direction Options

## Overview

**Client/Product:**
**Project Type:**
**Industry:**
**Prepared For:** Design direction selection before Design DNA

Three distinct visual directions are presented below. Choose one to proceed to Design DNA.

---

## Direction A: [Name]

**One-Line Personality:**
**Mood Keywords:**
**Color Territory:**
**Typography Personality:**
**Layout Philosophy:**
**Motion Personality:**
**Comparable Brands:**
**Why This Works For This Project:**
**What Makes It Distinctive:**
**What This Direction Avoids:**

---

## Direction B: [Name]

[Same structure]

---

## Direction C: [Name]

[Same structure]

---

## Selection Checkpoint

Which direction resonates most for this project?

- Reply **A** to select Direction A
- Reply **B** to select Direction B
- Reply **C** to select Direction C
- Reply with what you like from multiple directions for a **hybrid**
- Reply **NEW** to request a fourth direction

---

## Chosen Direction Summary

_This section is filled after selection._

**Selected Direction:**
**Name:**
**Core Personality:**
**Color Territory:**
**Typography Direction:**
**Layout Philosophy:**
**Key Differentiator:**
**Design DNA Starting Point:**
[Summary of what the Design DNA Skill should use as its foundation]
```

---

## Hybrid Direction Handling

If the user wants elements from multiple directions:

1. Identify which elements from each direction they want.
2. Check that the chosen elements are compatible (warm palette + editorial layout works; premium restraint + playful icons does not).
3. If compatible: create a hybrid direction profile and present it as Direction D.
4. If incompatible: explain the tension and ask which element takes priority.

---

## Project Memory Behavior

**Skill Number:** 03.5
**Skill Role:** Design Direction Selector — generates three directions, human picks one, feeds Design DNA.

Before running this skill:

1. Check whether `.agency/` exists.
2. Read `.agency/CURRENT_CONTEXT.md` first.
3. Read `.agency/CONTEXT_INDEX.json` second.
4. Read required context files below.
5. Do not proceed to Design DNA until direction is selected.

### Required Context Files For This Skill

- `.agency/CURRENT_CONTEXT.md`
- `.agency/CLIENT_BRIEF.md`
- `.agency/UX_STRATEGY.md`
- `.agency/COMPETITIVE_ANALYSIS.md` (if available)
- `.agency/PROJECT_STATE.json`

### Skill Output Files

- `.agency/DESIGN_DIRECTION_OPTIONS.md` — three direction profiles + chosen direction summary
- `.agency/PROJECT_STATE.json` — mark `design_direction` phase as complete
- `.agency/CURRENT_CONTEXT.md` — updated with chosen direction name
- `.agency/CONTEXT_INDEX.json` — updated
- `.agency/CHANGELOG.md` — append entry
- `.agency/DECISIONS.md` — record the chosen direction and rationale

---

## Session Resume Behavior

When starting in a new AI session:

1. Read `.agency/CURRENT_CONTEXT.md`.
2. Read `.agency/CONTEXT_INDEX.json`.
3. Check if `.agency/DESIGN_DIRECTION_OPTIONS.md` contains a chosen direction.
4. If chosen: confirm and proceed to Design DNA.
5. If options presented but not chosen: re-present options for selection.
6. If missing: rebuild from brief and UX strategy.

---

## Post-Task Update Behavior

After direction is selected:

1. Save the full document including chosen direction to `.agency/DESIGN_DIRECTION_OPTIONS.md`.
2. Update `.agency/CURRENT_CONTEXT.md`:
   - Add chosen direction name to Design Direction field
3. Update `.agency/PROJECT_STATE.json` — set `design_direction.status` to `complete`.
4. Update `.agency/CONTEXT_INDEX.json`:
   - Set `current_phase` to `design-direction`
   - Set `current_skill` to `design-dna`
   - Set `required_context_files` to `[".agency/CURRENT_CONTEXT.md", ".agency/CLIENT_BRIEF.md", ".agency/UX_STRATEGY.md", ".agency/DESIGN_DIRECTION_OPTIONS.md", ".agency/COMPETITIVE_ANALYSIS.md", ".agency/PROJECT_STATE.json"]`
5. Append entry to `.agency/CHANGELOG.md`.
6. Record chosen direction and reason in `.agency/DECISIONS.md`.
7. Do not delete previous entries.

---

## Example Trigger Phrases

- "Generate design directions."
- "Show me three visual concepts before we design."
- "What direction should this UI take?"
- "Create design direction options."
- "Let the client pick a visual direction."
- "Generate direction options before Design DNA."
- "What visual territory should we own?"
