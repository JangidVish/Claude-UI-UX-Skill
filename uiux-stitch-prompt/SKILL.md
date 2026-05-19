# Google Stitch Prompt Generator Skill

## Purpose

This skill converts a completed **Project UI Brief**, **UX Strategy Document**, and **Design DNA Document** into a polished, high-quality prompt for Google Stitch.

The goal is to help the team generate UI concepts that feel custom, premium, consistent, conversion-focused, and not obviously AI-generated.

The output of this skill is a ready-to-paste **Google Stitch Prompt**.

---

## When To Use This Skill

Use this skill after completing:

1. Client Discovery Skill
2. UX Strategy Skill
3. Design DNA Skill

Use it before:

- Generating UI concepts in Google Stitch
- Creating visual concept variations
- Asking Stitch for responsive layouts
- Creating first-pass page or screen designs

Do **not** use this skill before the project brief, UX strategy, and Design DNA are ready.

---

## Core Behavior

When this skill is triggered, act as a senior UI/UX prompt director and visual design strategist.

Your job is to:

1. Read the Project UI Brief.
2. Read the UX Strategy Document.
3. Read the Design DNA Document.
4. Identify the page or screen to generate.
5. Convert all strategic and visual rules into one clear Google Stitch prompt.
6. Include layout requirements.
7. Include design system rules.
8. Include content rules.
9. Include interaction and motion guidance.
10. Include anti-AI design rules.
11. Create a prompt that is specific, practical, and easy to paste into Google Stitch.

The prompt should help Google Stitch generate a strong first concept without requiring the designer to manually invent the layout.

---

## Required Input

This skill requires:

- Project UI Brief
- UX Strategy Document
- Design DNA Document
- Page/screen name to generate
- Target device type:
  - Desktop
  - Mobile
  - Responsive
  - Desktop-first responsive
  - Mobile-first responsive

Optional but helpful:

- Existing logo
- Brand colors
- Competitor references
- Inspiration links
- Existing website/app link
- Preferred content tone
- Required sections/components
- Animation preference
- Framework or handoff requirements

---

## Important Rules

### 1. Do Not Create Generic Prompts

Avoid weak prompts like:

```txt
Create a modern landing page for a SaaS company.
```

Create specific prompts like:

```txt
Create a desktop-first responsive landing page for a B2B AI research assistant aimed at startup founders and product teams. The UI should feel calm, intelligent, editorial, and premium, with a neutral base, restrained accent color, strong information hierarchy, realistic product copy, and subtle motion. Avoid purple-blue AI gradients, glowing orbs, generic SaaS cards, and fake dashboard visuals.
```

---

### 2. Always Include Context

Every Stitch prompt must include:

- What the product/business is
- Who the users are
- What the screen/page goal is
- What action the user should take
- What emotional response the UI should create

---

### 3. Always Include UX Structure

Do not ask Stitch to “make a page” without structure.

Include required sections or modules in order.

Example:

```txt
Include these sections in order:
1. Hero with clear value proposition and primary CTA
2. Trust strip with client logos or metrics
3. Problem section
4. Solution overview
5. Feature explanation
6. Process section
7. Testimonials
8. FAQ
9. Final CTA
```

---

### 4. Always Include Design DNA Rules

Every prompt must include:

- Visual positioning
- Color system guidance
- Typography direction
- Layout rules
- Component style
- Imagery/icon direction
- Motion direction
- Anti-patterns

---

### 5. Ask For Realistic Content

Avoid placeholder content.

Use:

```txt
Use realistic, industry-specific copy. Avoid lorem ipsum and generic placeholder text.
```

For example:

Bad:

```txt
Feature One, Feature Two, Feature Three
```

Better:

```txt
AI-powered brief generation, source-backed research summaries, collaborative review workspace
```

---

### 6. Control The “AI Look”

Always include an anti-AI section.

Common avoid rules:

- No purple-blue AI gradients unless brand requires them
- No glowing orbs
- No generic glassmorphism
- No random 3D objects
- No repeated 3-card layouts
- No fake dashboard charts unless the product requires dashboards
- No inconsistent border radius
- No random shadows
- No decorative blobs
- No generic startup hero

---

### 7. Make The Prompt Actionable

Google Stitch should be able to act on the prompt directly.

Avoid overly abstract language.

Bad:

```txt
Make it world-class and beautiful.
```

Better:

```txt
Use a 12-column desktop grid, generous section spacing, a clear hero hierarchy, restrained accent color for primary actions, realistic section copy, and consistent card radius across all components.
```

---

### 8. Include Variation Instructions When Needed

If creating multiple concepts, specify the variation type.

Examples:

- Concept A: Minimal premium
- Concept B: Editorial and image-led
- Concept C: Bold conversion-focused
- Concept D: Enterprise dashboard
- Concept E: Warm consumer app

---

### 9. Preserve The Design System

If refining an existing concept, instruct Stitch to keep the design system consistent.

Example:

```txt
Keep the same color palette, typography direction, spacing rhythm, button style, card radius, and brand tone. Improve layout hierarchy and originality without introducing new visual styles.
```

---

## Prompt Generation Process

Follow this process every time:

### Step 1: Confirm Screen/Page Target

Identify what the prompt should generate:

- Home page
- Landing page
- Pricing page
- Dashboard
- Admin panel
- Product detail page
- Checkout page
- Onboarding screen
- Mobile app home
- Settings screen
- Other

If not provided, ask:

```md
Which page or screen should this Stitch prompt generate first?
```

If the user wants to move fast, choose the most important first screen based on the UX Strategy.

---

### Step 2: Extract Project Context

From the Project UI Brief, extract:

- Client/product name
- Industry
- Target audience
- Business goal
- CTA
- Brand direction
- Competitors/inspiration
- Assets available

---

### Step 3: Extract UX Structure

From the UX Strategy Document, extract:

- Page/screen goal
- User journey
- Section order
- CTA strategy
- Trust elements
- Required states
- Mobile behavior

---

### Step 4: Extract Design DNA

From the Design DNA Document, extract:

- Visual positioning
- Emotional tone
- Color rules
- Typography direction
- Layout system
- Component style
- Imagery/icon style
- Motion principles
- Anti-AI rules

---

### Step 5: Create The Stitch Prompt

Use the output format below.

---

## Output Format

Always produce the final output in this format:

```md
# Google Stitch Prompt

Copy and paste this prompt into Google Stitch:

---

Create a [desktop/mobile/responsive/desktop-first responsive/mobile-first responsive] UI for **[client/product name]**, a [project/business description].

## Product Context

[Explain what the product/business does, who it serves, and why users come to this page/screen.]

## Target Audience

[Describe the users, their expectations, their pain points, and what they should feel while using the UI.]

## Page / Screen Goal

Design the **[page/screen name]**.

Primary goal:
[State the main user/business goal.]

Primary CTA:
[CTA text.]

Secondary CTA:
[CTA text, if any.]

## UX Structure

Use this section/module order:

1. [Section/module name] — [purpose]
2. [Section/module name] — [purpose]
3. [Section/module name] — [purpose]
4. [Section/module name] — [purpose]
5. [Section/module name] — [purpose]
6. [Section/module name] — [purpose]
7. [Section/module name] — [purpose]

## Visual Direction

The UI should feel:
[Describe the visual positioning and emotional tone.]

Design personality:
[Describe the personality from the Design DNA.]

Originality angle:
[Explain how the UI should avoid looking like a template.]

## Design System Rules

### Color

Use this color direction:
- Background:
- Surface:
- Primary text:
- Secondary text:
- Border:
- Primary accent:
- Secondary accent:
- Success/warning/error states:

Color usage rules:
- 
- 
- 

### Typography

Use this typography direction:
- Heading style:
- Body style:
- Label/caption style:
- Type hierarchy:
- Readability rules:

### Layout

Use this layout direction:
- Grid:
- Container:
- Section spacing:
- Alignment:
- Card density:
- Mobile stacking:

### Components

Use this component style:
- Buttons:
- Cards:
- Forms:
- Navigation:
- Badges/tags:
- Tables/charts, if needed:
- Modals/overlays, if needed:

### Imagery / Icons

Use this visual asset direction:
- Photography:
- Illustration:
- Icons:
- Image treatment:
- Avoid:

## Interaction & Motion

Use subtle, premium micro-interactions:
- Button hover:
- Card hover:
- Section reveal:
- Loading state:
- Success/error feedback:

Avoid bouncy, excessive, decorative, or slow animations.

## Content Rules

Use realistic, industry-specific copy.

Avoid:
- Lorem ipsum
- Generic placeholders
- Fake-sounding AI copy
- Repeated headings
- Empty feature labels like “Feature One”
- Unnecessary buzzwords

Make the content feel like a real product or client website.

## Anti-AI Design Rules

Avoid:
- 
- 
- 
- 
- 
- 

## Quality Bar

The output should feel like it was designed by a senior UI/UX designer for a premium agency.

It should be:
- Consistent
- Conversion-focused
- Visually disciplined
- Responsive-ready
- Human-crafted
- Not template-like
- Not obviously AI-generated
```

---

## Variation Prompt Format

Use this format when the user wants multiple design directions.

```md
# Google Stitch Concept Variation Prompts

Generate 3 different UI concepts for the same page.

---

## Concept A: [Name]

[Prompt with a specific visual direction.]

---

## Concept B: [Name]

[Prompt with a second visual direction.]

---

## Concept C: [Name]

[Prompt with a third visual direction.]

---

Important:
All concepts must follow the same business goal, UX structure, CTA strategy, and brand constraints, but they should explore different visual expressions.
```

---

## Refinement Prompt Format

Use this format when improving an existing Stitch result.

```md
# Google Stitch Refinement Prompt

Refine the previous UI concept.

## Keep

- 
- 
- 

## Improve

- 
- 
- 

## Fix

- 
- 
- 

## Remove / Avoid

- 
- 
- 

## Maintain Design System

Keep the same:
- Color palette
- Typography direction
- Spacing rhythm
- Button style
- Card radius
- Navigation structure
- Brand personality

## Updated Direction

[Describe exactly how the UI should improve.]

## Quality Instruction

Make the UI feel more intentional, human-designed, conversion-focused, and premium. Remove anything that feels generic, repetitive, or AI-generated.
```

---

## Prompt Patterns By Project Type

Use these patterns as starting points.

---

### A. Landing Page Prompt Pattern

Include:

- Hero
- Trust strip
- Problem
- Solution
- Benefits
- Proof
- Process
- Testimonials
- FAQ
- Final CTA

Key instruction:

```txt
Create strong conversion flow from first impression to final CTA. Make each section answer a user question and move the visitor closer to action.
```

---

### B. SaaS Dashboard Prompt Pattern

Include:

- Sidebar navigation
- Top command/search area
- Overview metrics
- Priority alerts
- Main work area
- Recent activity
- Suggested actions
- Empty/loading states

Key instruction:

```txt
Prioritize clarity, density control, information hierarchy, and repeat-use efficiency over decorative visuals.
```

---

### C. Admin Panel Prompt Pattern

Include:

- Sidebar
- Header
- Filters
- Search
- Table/list view
- Detail drawer
- Bulk actions
- Status indicators
- Confirmation states

Key instruction:

```txt
Design for operational speed, scanning, filtering, and clear actions.
```

---

### D. Ecommerce Prompt Pattern

Include:

- Product discovery
- Category or product grid
- Filters
- Product cards
- Product detail area
- Trust signals
- Cart CTA
- Reviews
- Shipping/return clarity

Key instruction:

```txt
Keep product visibility, price clarity, trust, and purchase action highly visible.
```

---

### E. Mobile App Prompt Pattern

Include:

- App header
- Main user action
- Bottom navigation
- Cards or content feed
- Primary flow
- Empty state
- Confirmation state

Key instruction:

```txt
Design thumb-friendly mobile interactions with clear hierarchy, minimal typing, and strong feedback.
```

---

## Quality Checklist

Before finalizing the Stitch prompt, check:

- [ ] Does the prompt include product context?
- [ ] Does it define the target audience?
- [ ] Does it define the page/screen goal?
- [ ] Does it include primary CTA?
- [ ] Does it include section/module order?
- [ ] Does it include visual direction?
- [ ] Does it include color rules?
- [ ] Does it include typography direction?
- [ ] Does it include layout rules?
- [ ] Does it include component style?
- [ ] Does it include imagery/icon rules?
- [ ] Does it include motion guidance?
- [ ] Does it request realistic content?
- [ ] Does it include anti-AI design rules?
- [ ] Is the prompt specific enough to paste directly into Google Stitch?

---

## Anti-Patterns To Avoid

Do not:

- Create vague prompts.
- Ignore the Design DNA.
- Ignore the UX Strategy.
- Ask for “beautiful” without defining what beautiful means.
- Ask Stitch to decide the whole structure from scratch.
- Include too many conflicting styles.
- Use multiple unrelated visual references.
- Overload the prompt with unnecessary jargon.
- Skip anti-AI rules.
- Skip realistic copy instruction.
- Skip mobile/responsive guidance.
- Generate final code in this skill.

---

## Example Trigger Phrases

Use this skill when the user says:

- “Generate the Stitch prompt.”
- “Create a prompt for Google Stitch.”
- “Turn this brief into a Stitch prompt.”
- “Make the final UI generation prompt.”
- “Prepare the prompt for the first concept.”
- “Create 3 concept prompts for Stitch.”
- “Make a refinement prompt for Stitch.”
- “Generate a desktop-first prompt.”
- “Generate a mobile app prompt.”
- “Create a prompt using the Design DNA.”

---

## Example Output

```md
# Google Stitch Prompt

Copy and paste this prompt into Google Stitch:

---

Create a desktop-first responsive landing page UI for **UrbanNest Interiors**, a premium residential interior design studio serving high-income homeowners.

## Product Context

UrbanNest Interiors helps premium homeowners design and execute refined, turnkey home interiors. Visitors are likely evaluating trust, taste, quality, and process before booking a consultation.

## Target Audience

The target audience is premium homeowners aged around 30–55 who want a beautiful, reliable, and stress-free interior design experience. They expect visual polish, proof of past work, process clarity, and a strong sense of trust.

## Page / Screen Goal

Design the **Landing Page**.

Primary goal:
Generate qualified consultation bookings.

Primary CTA:
Book a Consultation

Secondary CTA:
View Projects

## UX Structure

Use this section order:

1. Hero — communicate premium value proposition and consultation CTA
2. Trust Strip — show experience, project count, or client satisfaction metrics
3. Featured Projects — show visual proof through premium project cards
4. Service Benefits — explain what clients get beyond decoration
5. Process — explain how consultation to execution works
6. Testimonials — build trust through client voices
7. FAQ — resolve cost, timeline, and execution concerns
8. Final CTA — encourage booking a consultation

## Visual Direction

The UI should feel like a quiet luxury editorial website: spacious, refined, warm, aspirational, and trustworthy.

Design personality:
Premium, calm, image-led, confident, and polished.

Originality angle:
Use editorial section rhythm and large visual storytelling instead of generic icon-based service cards.

## Design System Rules

### Color

Use this color direction:
- Background: warm ivory
- Surface: soft white
- Primary text: deep charcoal
- Secondary text: warm grey
- Border: warm sand
- Primary accent: muted bronze
- Secondary accent: olive grey

Color usage rules:
- Use the accent color only for primary CTAs and important highlights.
- Keep most of the interface neutral and photography-led.
- Avoid loud gold, neon colors, and purple-blue gradients.

### Typography

Use this typography direction:
- Heading style: elegant editorial, confident, slightly high contrast
- Body style: clean, calm, readable sans-serif
- Label/caption style: small refined labels with generous spacing
- Type hierarchy: large hero headline, restrained section headings, comfortable body text
- Readability rules: avoid thin body text and low-opacity paragraphs

### Layout

Use this layout direction:
- Desktop-first responsive layout
- Spacious 12-column grid
- Generous section spacing
- Strong alignment
- Large image-led project sections
- Mobile should stack content clearly with CTA visible early

### Components

Use this component style:
- Buttons: refined, medium radius, clear hover states
- Cards: minimal, image-led, thin borders, soft or no shadows
- Forms: clean, calm, easy to complete
- Navigation: simple, premium, uncluttered
- Badges/tags: subtle, not colorful

### Imagery / Icons

Use this visual asset direction:
- Photography should feel premium, architectural, warm, and editorial
- Avoid generic stock images
- Use icons sparingly
- Prefer text and photography over decorative illustrations

## Interaction & Motion

Use subtle, premium micro-interactions:
- Button hover: slight brightness or border transition
- Card hover: subtle image scale or lift
- Section reveal: soft fade and upward movement
- Loading state: simple skeleton
- Success/error feedback: calm and clear

Avoid bouncy, excessive, decorative, or slow animations.

## Content Rules

Use realistic, industry-specific copy.

Avoid:
- Lorem ipsum
- Generic placeholders
- Fake-sounding AI copy
- Repeated headings
- Empty feature labels like “Feature One”
- Unnecessary buzzwords

Make the content feel like a real premium interior design studio.

## Anti-AI Design Rules

Avoid:
- Generic 3-card feature grids with random icons
- Purple-blue gradients
- Glassmorphism
- Decorative blobs
- Overuse of gold
- Repeating the same section rhythm
- Stock-photo-heavy generic sections
- Fake luxury patterns

## Quality Bar

The output should feel like it was designed by a senior UI/UX designer for a premium agency.

It should be:
- Consistent
- Conversion-focused
- Visually disciplined
- Responsive-ready
- Human-crafted
- Not template-like
- Not obviously AI-generated
```

---

## Project Memory Behavior

**Skill Number:** 04
**Skill Role:** Stitch Prompt Generator — reads brief, UX strategy, and Design DNA, produces Google Stitch prompt.

Before running this skill:

1. Check whether `.agency/` exists.
2. If `.agency/` does not exist, ask the user to run the Client Discovery Skill first.
3. Read `.agency/CURRENT_CONTEXT.md` first.
4. Read `.agency/CONTEXT_INDEX.json` second.
5. Read only the required context files listed below.
6. Do not read every `.md` file by default.
7. Do not restart the project from zero.
8. Preserve previous decisions.

### Required Context Files For This Skill

- `.agency/CURRENT_CONTEXT.md`
- `.agency/CLIENT_BRIEF.md`
- `.agency/UX_STRATEGY.md`
- `.agency/DESIGN_DNA.md`

### Skill Output Files

After completing this skill, write output to:

- `.agency/STITCH_PROMPT.md` — the Google Stitch Prompt
- `.agency/PROJECT_STATE.json` — updated state
- `.agency/CURRENT_CONTEXT.md` — updated session context
- `.agency/CONTEXT_INDEX.json` — updated index
- `.agency/CHANGELOG.md` — append entry
- `.agency/TODO.md` — update next steps

---

## Session Resume Behavior

When starting in a new AI session:

1. Do not ask the user to repeat the full project context.
2. Read `.agency/CURRENT_CONTEXT.md`.
3. Read `.agency/CONTEXT_INDEX.json`.
4. Read only the files listed under `required_context_files`.
5. Summarize:
   - What the project is
   - What phase it is in
   - What has been completed
   - What is currently in progress
   - What the current task is
   - What must not be changed
6. Continue from the current state.

---

## Post-Task Update Behavior

After completing this skill:

1. Save the Google Stitch Prompt to `.agency/STITCH_PROMPT.md`.
2. Update `.agency/CURRENT_CONTEXT.md` with current phase, completed items, and next step.
3. Update `.agency/PROJECT_STATE.json`.
4. Update `.agency/CONTEXT_INDEX.json`:
   - Set `current_phase` to `stitch-prompt`
   - Set `current_skill` to `ui-critique`
   - Set `required_context_files` to `[".agency/CURRENT_CONTEXT.md", ".agency/DESIGN_DNA.md", ".agency/STITCH_PROMPT.md", ".agency/PROJECT_STATE.json"]`
5. Append a short entry to `.agency/CHANGELOG.md`.
6. Update `.agency/TODO.md` with next steps.
7. Add any major prompt decisions to `.agency/DECISIONS.md`.
8. Do not delete previous decisions or changelog entries.
