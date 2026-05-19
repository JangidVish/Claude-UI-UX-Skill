---
skill_id: uiux-competitive-analysis
skill_number: 00
requires_visual_input: false
requires_browser: true
project_complexity: standard, full
human_checkpoint_after: false
output_file: .agency/COMPETITIVE_ANALYSIS.md
runs_before: uiux-client-discovery
---

# Competitive Analysis Skill

## Purpose

This skill uses browser automation to visit, screenshot, and analyze competitor websites before any design work begins.

The goal is to understand what the competition looks like, identify layout patterns common in the industry, find visual and UX gaps, and define a clear differentiation strategy before writing the Design DNA.

The output is a structured **Competitive Analysis Report** that feeds directly into:

- Design DNA Skill (originality angle)
- Design Direction Selector Skill (what to avoid and what to beat)
- Google Stitch / UI Generation Prompt Skill (competitive context)

---

## When To Use

Use this skill:

- Before or alongside Client Discovery
- Before Design DNA
- When the brief includes competitor or inspiration URLs
- When the team needs to understand the visual landscape before designing
- When the client asks "how do we stand out from X, Y, Z?"

Skip this skill only for lite projects with no competitor references.

---

## Core Behavior

When this skill is triggered, act as a senior UX researcher and visual design strategist.

Use browser automation tools to visit each competitor URL, take screenshots, and analyze the live site.

Your job is to:

1. Read competitor URLs from `.agency/CLIENT_BRIEF.md` or ask if not available.
2. Visit each competitor site using browser tools.
3. Screenshot the homepage and one key inner page if relevant.
4. Analyze each site across all criteria below.
5. Identify patterns shared across competitors.
6. Identify gaps and weaknesses in competitor UIs.
7. Define the differentiation opportunity.
8. Produce the Competitive Analysis Report.

---

## Browser Automation Instructions

Use the Playwright browser tools available in this environment.

For each competitor URL:

**Step 1 — Navigate**
Use `browser_navigate` to open the competitor URL.

**Step 2 — Screenshot**
Use `browser_take_screenshot` to capture the full page or viewport.

**Step 3 — Analyze**
Review the screenshot visually and analyze:

- Above-the-fold layout
- Hero section structure
- Color palette and dominant colors
- Typography style
- Navigation pattern
- CTA placement and style
- Section rhythm and layout patterns
- Image and illustration style
- Spacing density
- Component patterns (cards, grids, etc.)
- Trust signals
- Mobile readiness indicators

**Step 4 — Repeat** for each competitor (maximum 5 sites).

If browser tools are unavailable, ask the user to describe each competitor site or paste screenshots.

---

## Required Input

From `.agency/CLIENT_BRIEF.md`:

- Competitor URLs (Section: Main Competitors)
- Inspiration references (Section: Inspiration References)
- Project type
- Target audience
- Desired brand feel

If competitor URLs are missing from the brief, ask:

```
No competitor URLs found in the brief. Please provide 2–5 competitor or inspiration site URLs to analyze.

Or type SKIP to proceed without competitive analysis.
```

If the user types SKIP, note in the report:
```
Competitive analysis was skipped. Design DNA originality angle will be based on industry patterns only.
```

---

## Analysis Criteria

For each competitor site, evaluate:

### 1. Visual Positioning
- What does the site communicate in the first 3 seconds?
- Does it feel premium, generic, corporate, playful, technical?
- What industry archetype does it follow?

### 2. Color System
- Dominant background color
- Primary accent color
- Does it use gradients? Which type?
- Does it follow a disciplined palette or feel chaotic?

### 3. Typography
- Serif, sans-serif, or mixed?
- Editorial feel vs corporate feel?
- Is hierarchy clear?
- Font weight usage

### 4. Layout Pattern
- Hero layout: centered, split, full-bleed image?
- Section rhythm: repeated cards, editorial variety, mixed?
- Grid: tight or spacious?
- Whitespace usage

### 5. Navigation
- Style: minimal, mega-menu, sticky?
- CTA in nav: yes/no?
- Mobile nav: visible or not

### 6. CTA Strategy
- Primary CTA text and placement
- How many CTAs visible above fold?
- CTA visual weight

### 7. AI-Generated Smell
- Does it look AI-generated or template-like?
- Purple-blue gradients?
- Generic 3-card feature grids?
- Glassmorphism?

### 8. Trust Signals
- What trust elements are visible?
- Logos, testimonials, metrics, certifications?

### 9. Weaknesses
- What is clearly missing?
- What is done poorly?
- What would frustrate the target user?

### 10. Strengths
- What does this competitor do better than average?

---

## Pattern Extraction

After analyzing all competitors:

**Common Patterns** — What do all or most competitors do the same way?
These are industry conventions. Follow them only when breaking them would confuse users.

**Common Weaknesses** — What do most competitors do poorly?
These are differentiation opportunities.

**Visual Fatigue Patterns** — What design elements are overused in this industry?
These should be avoided or subverted.

**Unoccupied Positioning** — What visual or UX territory does no competitor own?
This is where the new design should aim.

---

## Output Format

```md
# Competitive Analysis Report

## 1. Analysis Overview

**Client/Product:**
**Industry:**
**Project Type:**
**Competitors Analyzed:**
**Analysis Date:**

---

## 2. Competitor Profiles

### Competitor 1: [Name]

**URL:**
**Screenshot:** [captured / not available]
**First Impression:**

**Visual Positioning:**
**Color System:**
**Typography:**
**Layout Pattern:**
**Navigation:**
**CTA Strategy:**
**Trust Signals:**
**AI-Generated Smell:** Yes / No / Partial

**Strengths:**
-
-

**Weaknesses:**
-
-

---

### Competitor 2: [Name]

[Same structure]

---

### Competitor 3: [Name]

[Same structure]

---

## 3. Pattern Analysis

### Common Patterns Across Competitors

-
-
-

### Common Weaknesses

-
-
-

### Visual Fatigue Patterns (Overused)

-
-
-

### Unoccupied Visual Territory

-
-
-

---

## 4. Differentiation Strategy

**What Our Design Must Do Differently:**
-
-
-

**Visual Territory To Own:**

**What To Avoid (Used By All Competitors):**
-
-
-

**Originality Angle:**

---

## 5. Design DNA Input

Feed these findings into Design DNA Skill:

**Originality Angle:**
**Anti-Patterns To Avoid:**
**Color Territory Available:**
**Typography Gap:**
**Layout Opportunity:**

---

## 6. Recommended Next Step

Run the **Client Discovery Skill** if not yet complete, or proceed to **UX Strategy Skill**.
```

---

## Lite Mode Behavior

If `project_complexity` in `PROJECT_STATE.json` is `lite`:

- Analyze maximum 2 competitors
- Use shorter analysis format
- Skip Pattern Analysis section
- Produce a brief summary only

---

## Project Memory Behavior

**Skill Number:** 00
**Skill Role:** Competitive Analysis — runs before or alongside discovery to inform design direction.

Before running this skill:

1. Check whether `.agency/` exists.
2. Read `.agency/CURRENT_CONTEXT.md` first if it exists.
3. Read `.agency/CONTEXT_INDEX.json` second.
4. Read `.agency/CLIENT_BRIEF.md` for competitor URLs.
5. Check `project_complexity` in `.agency/PROJECT_STATE.json` — if `lite`, run abbreviated analysis.

### Required Context Files For This Skill

- `.agency/CURRENT_CONTEXT.md`
- `.agency/CLIENT_BRIEF.md`
- `.agency/PROJECT_STATE.json`

### Skill Output Files

- `.agency/COMPETITIVE_ANALYSIS.md` — the full report
- `.agency/PROJECT_STATE.json` — mark `competitive_analysis` phase as complete
- `.agency/CURRENT_CONTEXT.md` — updated
- `.agency/CONTEXT_INDEX.json` — updated
- `.agency/CHANGELOG.md` — append entry

---

## Session Resume Behavior

When starting in a new AI session:

1. Read `.agency/CURRENT_CONTEXT.md`.
2. Read `.agency/CONTEXT_INDEX.json`.
3. Read `.agency/CLIENT_BRIEF.md` for competitor URLs.
4. Continue analysis from where it stopped.
5. Do not re-analyze competitors already documented in `.agency/COMPETITIVE_ANALYSIS.md`.

---

## Post-Task Update Behavior

After completing this skill:

1. Save report to `.agency/COMPETITIVE_ANALYSIS.md`.
2. Update `.agency/CURRENT_CONTEXT.md`.
3. Update `.agency/PROJECT_STATE.json` — set `competitive_analysis.status` to `complete`.
4. Update `.agency/CONTEXT_INDEX.json` — set `required_context_files` for next skill.
5. Append entry to `.agency/CHANGELOG.md`.
6. Add differentiation decisions to `.agency/DECISIONS.md`.
7. Do not delete previous entries.

---

## Example Trigger Phrases

- "Analyze competitors before we start designing."
- "Run competitive analysis."
- "Screenshot and review these competitor sites."
- "What does the competition look like?"
- "Find design gaps in the market."
- "Analyze these URLs before we design."
