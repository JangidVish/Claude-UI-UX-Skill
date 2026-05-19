---
skill_id: uiux-wireframe-ia
skill_number: 02.5
requires_visual_input: false
requires_browser: false
project_complexity: standard, full
human_checkpoint_after: true
output_file: .agency/WIREFRAMES.md
runs_between: uiux-strategy-skill, uiux-desig-dna
---

# Wireframe & IA Validation Skill

## Purpose

This skill converts a completed **UX Strategy Document** into text-based wireframes and a validated information architecture before any visual design begins.

The goal is to test structure, content priority, and layout logic at zero visual cost — before color, typography, or visual DNA locks anything in.

Problems caught here cost nothing to fix. Problems caught after visual design cost hours.

The output is a **Wireframe & IA Validation Document** that becomes the foundation for:

- Design DNA Skill
- UI Generation Prompt Skill
- Developer Handoff Skill

---

## When To Use

Use this skill after:

1. Client Discovery Skill
2. UX Strategy Skill

Use it before:

- Design DNA Skill
- Design Direction Selector Skill
- Any visual UI generation

Skip only for lite projects or when the UX Strategy already contains detailed section-level specifications.

---

## Core Behavior

When this skill is triggered, act as a senior information architect and interaction designer.

Your job is to:

1. Read the UX Strategy Document.
2. Read the Project UI Brief for page list and content requirements.
3. Convert section order into text wireframes for each page or screen.
4. Define content priority within each section.
5. Define layout pattern for each section (not visual style — only structure).
6. Define navigation structure.
7. Define mobile stacking order.
8. Flag structural risks.
9. Present wireframes for human review before proceeding.
10. Produce the Wireframe & IA Validation Document.

---

## Important Rules

### 1. No Visual Design In This Skill

Do not define colors, fonts, gradients, or any visual property.

Allowed:
- Layout position (left, right, center, full-width)
- Content blocks (headline, subheadline, image, CTA, list)
- Column count (2-col, 3-col, full-width)
- Content priority (primary, secondary, tertiary)
- Interaction hint (sticky, collapsible, expandable)

Not allowed:
- Color choices
- Font choices
- Shadow or border style
- Specific imagery direction

### 2. Use ASCII Wireframe Format

ASCII wireframes are readable in any text editor, AI tool, or document.

Primary format:

```
[ELEMENT: content description]
```

Examples:

```
[NAV: Logo left | Links center | CTA Button right]
[HERO: H1 Headline | Subtext | Primary CTA | Secondary CTA | Hero Image right]
[TRUST STRIP: Client Logo × 5 | horizontal scroll on mobile]
[FEATURE: Image left 50% | H2 + Body + Link right 50%]
[FEATURE: H2 + Body + Link left 50% | Image right 50% — alternating]
[TESTIMONIAL: Quote | Name + Role | Avatar | 3-col grid]
[CTA BLOCK: H2 | Subtext | Primary CTA | full-width background]
[FOOTER: Logo | Nav links | Legal | Social icons]
```

### 3. Include Mobile Stacking Order

For every multi-column section, define mobile stacking:

```
Desktop: [Image left 50%] [Content right 50%]
Mobile:  [Content] → [Image] → [CTA]
```

### 4. Human Checkpoint After This Skill

This skill always ends with a human review request:

```
Wireframes are ready for review.

Before proceeding to Design DNA, please confirm:
- [ ] Section order is correct
- [ ] Content priority is correct
- [ ] No sections are missing
- [ ] Mobile stacking order makes sense

Reply APPROVED to proceed to Design DNA Skill.
Reply with changes to adjust the wireframe.
```

Do not proceed to Design DNA until the user approves.

### 5. Flag Structural Risks

Identify problems that cannot be solved with visual design alone.

Examples:
- Too many sections make the page feel heavy
- CTA appears too late in the flow
- Trust signals missing in the first viewport
- Navigation has too many items
- Form appears before sufficient trust is built
- Mobile stacking puts image before CTA when CTA should be first

---

## Wireframe Process

### Step 1: Read UX Strategy

Extract:
- Page/screen list
- Section order per page
- CTA strategy
- Trust element placement
- Mobile UX notes

### Step 2: Read Project UI Brief

Extract:
- Required pages
- Required sections
- Required features
- Content assets available

### Step 3: Build Page Wireframes

For each page or screen:

1. Start with navigation
2. Follow section order from UX Strategy
3. Define layout pattern for each section
4. Note content type in each block
5. Add mobile stacking order
6. Add interaction hints where relevant

### Step 4: Build Navigation Structure

Define:
- Primary navigation items
- Secondary navigation
- CTA in nav
- Mobile nav behavior
- Footer structure

### Step 5: Flag Risks

Review the full wireframe set and identify:
- Conversion risks
- Content flow problems
- Mobile usability risks
- Missing trust elements
- Overloaded sections

### Step 6: Present For Approval

Always present wireframes and wait for approval before writing the output file.

---

## Wireframe Patterns By Project Type

### Landing Page

```
[NAV: Logo | Links | Primary CTA]
[HERO: H1 + Value Prop | Subtext | Primary CTA | Secondary Link | Visual right]
[TRUST STRIP: Logos or Metrics — full width]
[PROBLEM: H2 | 2–3 pain point cards or statements]
[SOLUTION: H2 | Subtext | 3-col benefit grid or split layout]
[PROOF: H2 | 2–3 case study cards or quote blocks]
[PROCESS: H2 | 3–4 step timeline or numbered list]
[TESTIMONIALS: 3-col quote cards or carousel]
[FAQ: H2 | Accordion list]
[FINAL CTA: H2 | Subtext | Primary CTA | full-width]
[FOOTER: Logo | Links | Legal]
```

### SaaS Dashboard

```
[SIDEBAR: Logo | Nav items | User account]
[TOPBAR: Page title | Search | Actions | User avatar]
[OVERVIEW STRIP: 4 metric cards — full width]
[PRIORITY AREA: Alert list left 40% | Main chart right 60%]
[DATA TABLE: Filters | Search | Column headers | Rows | Pagination]
[EMPTY STATE: Icon | Message | Primary action CTA]
```

### Admin Panel

```
[SIDEBAR: Logo | Nav sections | Collapse toggle]
[TOPBAR: Breadcrumb | Search | Filters | Actions]
[TABLE: Column headers | Status badges | Actions per row | Bulk select]
[DETAIL DRAWER: Header | Fields | Edit/Save actions | Close]
[CONFIRMATION MODAL: Warning message | Confirm | Cancel]
```

### Ecommerce

```
[NAV: Logo | Search | Cart | Account | Category links]
[HERO BANNER: Seasonal offer | Shop CTA]
[CATEGORY GRID: 3–4 col category tiles]
[PRODUCT GRID: Filters sidebar | 3-col product cards | Pagination]
[PRODUCT DETAIL: Image gallery left | Title + Price + Variants + CTA right]
[TRUST STRIP: Shipping | Returns | Security]
[CHECKOUT: Progress steps | Form fields | Order summary | Submit CTA]
```

### Mobile App

```
[STATUS BAR]
[HEADER: Back button | Title | Action icon]
[HERO/SUMMARY: Key info card]
[ACTION SECTION: Primary action button — full width]
[LIST/FEED: Card items — vertical scroll]
[BOTTOM NAV: 4–5 icon tabs with labels]
```

---

## Output Format

```md
# Wireframe & IA Validation Document

## 1. Document Overview

**Client/Product:**
**Project Type:**
**Pages Wireframed:**
**Wireframe Status:** Draft — Awaiting Approval

---

## 2. Navigation Structure

**Primary Navigation:**
-
-

**Mobile Navigation:**
-

**Footer Structure:**
-
-

---

## 3. Page Wireframes

### Page: [Name]

**Primary Goal:**
**Primary CTA:**

**Desktop Wireframe:**

```
[NAV: ...]
[SECTION: ...]
[SECTION: ...]
[FOOTER: ...]
```

**Mobile Stacking Order:**
1.
2.
3.

**Content Priority:**
- Primary:
- Secondary:
- Tertiary:

**Interaction Notes:**
-
-

---

### Page: [Name]

[Same structure repeated]

---

## 4. Structural Risks

-
-
-

---

## 5. IA Validation Notes

**Navigation Clarity:**
**Content Flow:**
**CTA Placement Logic:**
**Trust Signal Placement:**
**Mobile Usability:**

---

## 6. Human Review Checkpoint

Wireframes are ready for review.

Before proceeding to Design DNA, please confirm:

- [ ] Section order is correct
- [ ] Content priority is correct
- [ ] No sections are missing
- [ ] Mobile stacking order is logical
- [ ] CTA placement makes sense
- [ ] Trust signals appear early enough

Reply **APPROVED** to proceed to Design DNA Skill.
Reply with changes to adjust the wireframe.

---

## 7. Recommended Next Step

After approval: Run the **Design Direction Selector Skill** or the **Design DNA Skill**.
```

---

## Project Memory Behavior

**Skill Number:** 02.5
**Skill Role:** Wireframe & IA Validation — validates page structure before visual design locks in.

Before running this skill:

1. Check whether `.agency/` exists.
2. Read `.agency/CURRENT_CONTEXT.md` first.
3. Read `.agency/CONTEXT_INDEX.json` second.
4. Read only the required context files below.
5. Do not read every `.md` file.
6. Do not proceed to Design DNA before human approval.

### Required Context Files For This Skill

- `.agency/CURRENT_CONTEXT.md`
- `.agency/UX_STRATEGY.md`
- `.agency/CLIENT_BRIEF.md`
- `.agency/PROJECT_STATE.json`

### Skill Output Files

- `.agency/WIREFRAMES.md` — wireframes and IA document
- `.agency/PROJECT_STATE.json` — mark `wireframes` phase as complete
- `.agency/CURRENT_CONTEXT.md` — updated
- `.agency/CONTEXT_INDEX.json` — updated
- `.agency/CHANGELOG.md` — append entry

---

## Session Resume Behavior

When starting in a new AI session:

1. Read `.agency/CURRENT_CONTEXT.md`.
2. Read `.agency/CONTEXT_INDEX.json`.
3. Check if `.agency/WIREFRAMES.md` already exists and has an approval status.
4. If approved: proceed to Design DNA.
5. If unapproved draft: present wireframes again for review.
6. If missing: rebuild from UX Strategy.

---

## Post-Task Update Behavior

After approval and completing this skill:

1. Save approved wireframes to `.agency/WIREFRAMES.md`.
2. Update `.agency/CURRENT_CONTEXT.md`.
3. Update `.agency/PROJECT_STATE.json` — set `wireframes.status` to `complete`.
4. Update `.agency/CONTEXT_INDEX.json`:
   - Set `current_phase` to `wireframes`
   - Set `current_skill` to `design-direction` or `design-dna`
   - Set `required_context_files` to `[".agency/CURRENT_CONTEXT.md", ".agency/CLIENT_BRIEF.md", ".agency/UX_STRATEGY.md", ".agency/WIREFRAMES.md", ".agency/PROJECT_STATE.json"]`
5. Append entry to `.agency/CHANGELOG.md`.
6. Add any structural decisions to `.agency/DECISIONS.md`.
7. Do not delete previous entries.

---

## Example Trigger Phrases

- "Create wireframes for this project."
- "Validate the IA before we design."
- "Build text wireframes from the UX strategy."
- "Show me the layout structure before visual design."
- "Plan the page structure."
- "Wireframe the landing page."
- "Check the information architecture."
