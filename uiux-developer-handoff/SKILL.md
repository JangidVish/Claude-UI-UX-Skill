# Developer Handoff Skill

## Purpose

This skill converts an approved UI/UX concept into a practical, implementation-ready developer handoff document.

The goal is to help developers understand the final design direction, design tokens, reusable components, responsive behavior, interaction states, accessibility notes, content requirements, asset requirements, CMS needs, and implementation risks before development starts.

The output of this skill is a structured **Developer Handoff Document**.

---

## When To Use This Skill

Use this skill after:

1. Client Discovery Skill
2. UX Strategy Skill
3. Design DNA Skill
4. Google Stitch Prompt Generator Skill
5. UI Critique Skill
6. Humanization & Refinement Skill
7. Responsive + Accessibility Review Skill

Use it when:

- Final UI concept is selected.
- Design direction is approved.
- Developers need build instructions.
- Project is moving from design to implementation.
- Team needs a shared reference for components, states, and responsive rules.

Do **not** use this skill before the final UI direction is stable.

---

## Core Behavior

When this skill is triggered, act as a senior product designer, design systems lead, and frontend handoff specialist.

Your job is to:

1. Summarize the approved UI direction.
2. Extract design tokens.
3. Define reusable components.
4. Document page/screen structure.
5. Define responsive behavior.
6. Define interaction states.
7. Define animation behavior.
8. Define accessibility notes.
9. Define content and asset requirements.
10. Define CMS or dynamic content requirements.
11. Define implementation risks.
12. Create a clear checklist developers can follow.

The output should be practical, clear, and build-oriented.

---

## Required Input

This skill works best with:

- Final approved UI screenshot/concept
- Project UI Brief
- UX Strategy Document
- Design DNA Document
- Responsive + Accessibility Review Report
- Target framework/platform
- CMS requirement, if any
- Animation expectations
- Final page/screen list
- Asset list

Minimum required input:

- Final UI concept or description
- Project type
- Target platform/framework
- Required pages/screens

If information is missing, create the handoff with assumptions and mark them clearly.

---

## Important Rules

### 1. Make The Handoff Practical

Avoid vague handoff notes.

Bad:

```md
Make the website responsive and modern.
```

Better:

```md
Use a max-width container of 1200px on desktop, 24px side padding on tablet, and 16px side padding on mobile. Collapse 3-column sections into one column below 768px.
```

### 2. Extract Reusable Components

Every handoff should identify reusable components such as:

- Header
- Footer
- Hero
- Button
- Card
- Form input
- Testimonial block
- Pricing card
- Feature block
- FAQ accordion
- Modal
- Table
- Badge
- Sidebar
- Empty state
- Toast notification

### 3. Include Design Tokens

Document:

- Colors
- Typography
- Spacing
- Radius
- Shadows
- Borders
- Breakpoints
- Motion timings

If exact values are unknown, provide recommended starting values and mark them as assumptions.

### 4. Define States

Developers need states, not only static screens.

Include:

- Default
- Hover
- Focus
- Active
- Disabled
- Loading
- Empty
- Error
- Success
- Selected
- Expanded/collapsed

### 5. Include Responsive Rules

Document how each major layout adapts across:

- Desktop
- Tablet
- Mobile

Use specific rules.

Examples:

```md
- Hero: two-column layout on desktop, stacked text-first layout on mobile.
- Feature grid: 3 columns desktop, 2 columns tablet, 1 column mobile.
- Sidebar: persistent on desktop, drawer on tablet/mobile.
- Table: full table desktop, card list below 768px.
```

### 6. Include Accessibility Notes

Document:

- Heading hierarchy
- Keyboard navigation
- Focus states
- Form labels
- Error messages
- Alt text
- Color contrast
- Reduced motion
- ARIA needs where relevant

Do not claim full legal compliance unless formally audited.

### 7. Include Content And Asset Gaps

Developers should know what assets are needed.

Examples:

- Logo files
- Brand fonts
- Hero images
- Product screenshots
- Testimonials
- Case studies
- Icons
- Video embeds
- Final copy
- Legal links
- SEO metadata

### 8. Include Implementation Risks

Call out anything that may create build issues.

Examples:

- Heavy animations may affect performance.
- Missing images may reduce design quality.
- CMS content may break layout if text length varies.
- Tables may require special mobile handling.
- Third-party widgets may not match design system.
- Complex filtering may require backend support.

---

## Handoff Process

Follow this process every time:

1. Identify project context.
2. Summarize final design direction.
3. Extract design tokens.
4. Define reusable components.
5. Define page/screen structure.
6. Define responsive rules.
7. Define interaction states.
8. Define accessibility notes.
9. Define content and asset requirements.
10. Define CMS or dynamic content notes.
11. Define performance notes.
12. Define implementation risks.
13. Produce final developer checklist.

---

## Output Format

Always produce the final output in this format:

```md
# Developer Handoff Document

## 1. Project Summary

**Client/Product:**  
**Project Type:**  
**Platform/Framework:**  
**CMS Requirement:**  
**Primary User Action:**  
**Primary Business Goal:**  
**Final Design Status:**  

---

## 2. Final Design Direction

**Visual Style:**  
**Brand Feel:**  
**UX Approach:**  
**Layout Style:**  
**Component Style:**  
**Motion Style:**  
**Accessibility Priority:**  

---

## 3. Design Tokens

### Colors

| Token | Value | Usage |
|---|---:|---|
| `--color-bg` |  | Main background |
| `--color-surface` |  | Cards/forms |
| `--color-surface-elevated` |  | Elevated panels |
| `--color-text-primary` |  | Main text/headings |
| `--color-text-secondary` |  | Supporting text |
| `--color-text-muted` |  | Captions/metadata |
| `--color-border` |  | Borders/dividers |
| `--color-primary` |  | Primary CTA/accent |
| `--color-primary-hover` |  | Primary CTA hover |
| `--color-success` |  | Success states |
| `--color-warning` |  | Warning states |
| `--color-error` |  | Error states |
| `--color-info` |  | Info states |

### Typography

| Token | Value | Usage |
|---|---|---|
| `--font-heading` |  | Headings |
| `--font-body` |  | Body text |
| `--text-xs` |  | Captions |
| `--text-sm` |  | Labels |
| `--text-base` |  | Body |
| `--text-lg` |  | Large body |
| `--text-xl` |  | Small headings |
| `--text-2xl` |  | Section headings |
| `--text-4xl` |  | Hero headings |
| `--line-height-body` |  | Body readability |
| `--line-height-heading` |  | Heading readability |

### Spacing

| Token | Value | Usage |
|---|---:|---|
| `--space-1` | 4px | Micro spacing |
| `--space-2` | 8px | Small spacing |
| `--space-3` | 12px | Form spacing |
| `--space-4` | 16px | Base spacing |
| `--space-6` | 24px | Card spacing |
| `--space-8` | 32px | Section inner spacing |
| `--space-12` | 48px | Section spacing |
| `--space-16` | 64px | Large section spacing |
| `--space-24` | 96px | Hero/major section spacing |

### Radius

| Token | Value | Usage |
|---|---:|---|
| `--radius-sm` |  | Inputs/small elements |
| `--radius-md` |  | Buttons |
| `--radius-lg` |  | Cards |
| `--radius-xl` |  | Large panels |

### Shadows

| Token | Value | Usage |
|---|---|---|
| `--shadow-sm` |  | Small hover |
| `--shadow-md` |  | Cards |
| `--shadow-lg` |  | Modals |

### Breakpoints

| Token | Value |
|---|---:|
| `--bp-sm` | 640px |
| `--bp-md` | 768px |
| `--bp-lg` | 1024px |
| `--bp-xl` | 1280px |

### Motion

| Token | Value | Usage |
|---|---:|---|
| `--motion-fast` | 120ms | Button hover |
| `--motion-base` | 200ms | Cards/inputs |
| `--motion-slow` | 320ms | Modals/reveals |
| `--ease-standard` | ease-out | General motion |

---

## 4. Component Inventory

| Component | Purpose | Variants | Required States | Responsive Notes |
|---|---|---|---|---|
| Header |  |  | Default, sticky, mobile open |  |
| Footer |  |  | Default |  |
| Button |  | Primary, secondary, ghost | Default, hover, focus, active, disabled, loading |  |
| Card |  | Default, featured, compact | Default, hover, selected |  |
| Form Input |  | Text, email, phone, select, textarea | Default, focus, error, disabled, success |  |
| Hero |  |  |  |  |
| CTA Block |  |  |  |  |
| FAQ Accordion |  |  | Collapsed, expanded, focus |  |
| Modal / Drawer |  |  | Open, close, loading |  |
| Toast / Alert |  | Success, error, warning, info | Visible, dismissed |  |

---

## 5. Page / Screen Structure

### Page/Screen 1: [Name]

**Purpose:**  
**Primary CTA:**  
**Secondary CTA:**  

**Sections:**

1. 
2. 
3. 
4. 
5. 

**Interactions:**

- 
- 
- 

**Responsive Behavior:**

- Desktop:
- Tablet:
- Mobile:

**Content Needed:**

- 
- 
- 

---

### Page/Screen 2: [Name]

**Purpose:**  
**Primary CTA:**  
**Secondary CTA:**  

**Sections:**

1. 
2. 
3. 
4. 
5. 

**Interactions:**

- 
- 
- 

**Responsive Behavior:**

- Desktop:
- Tablet:
- Mobile:

**Content Needed:**

- 
- 
- 

---

## 6. Responsive Rules

### Desktop

- 
- 
- 

### Tablet

- 
- 
- 

### Mobile

- 
- 
- 

### Component-Specific Responsive Rules

- 
- 
- 

---

## 7. Interaction & State Requirements

### Buttons

- Default:
- Hover:
- Focus:
- Active:
- Disabled:
- Loading:

### Links

- Default:
- Hover:
- Focus:
- Active:

### Forms

- Default:
- Focus:
- Error:
- Success:
- Disabled:
- Loading:

### Navigation

- Desktop:
- Mobile:
- Active state:
- Open/close state:

### Feedback

- Toast:
- Inline alert:
- Success message:
- Error message:

### Content States

- Loading:
- Empty:
- No results:
- Error:
- Permission denied:

---

## 8. Animation Notes

**Animation Level:**  

**Allowed Animations:**  
- 
- 
- 

**Avoid:**  
- 
- 
- 

**Reduced Motion Rule:**  
Use reduced-motion fallback for users who prefer less motion.

---

## 9. Accessibility Notes

**Heading Structure:**  
**Keyboard Navigation:**  
**Focus States:**  
**Form Labels:**  
**Error Messages:**  
**Alt Text:**  
**ARIA Needs:**  
**Color Contrast:**  
**Touch Targets:**  
**Reduced Motion:**  

---

## 10. Content & Asset Requirements

### Available Assets

- 
- 
- 

### Missing Assets

- 
- 
- 

### Required Before Development

- 
- 
- 

### Copy Requirements

- Final hero copy:
- CTA labels:
- Section headings:
- Form labels:
- Error/success messages:
- SEO title/meta:
- Legal links:

---

## 11. CMS / Dynamic Content Notes

Use this section if CMS or dynamic content is required.

**CMS Collections:**  
- 
- 
- 

**Editable Fields:**  
- 
- 
- 

**Content Length Rules:**  
- 
- 
- 

**Fallback Rules:**  
- 
- 
- 

---

## 12. Performance Notes

**Image Optimization:**  
**Video Handling:**  
**Animation Performance:**  
**Font Loading:**  
**Third-Party Scripts:**  
**Core Web Vitals Risks:**  

---

## 13. Implementation Risks

- Risk 1:
- Risk 2:
- Risk 3:

---

## 14. Developer Questions To Resolve

1. 
2. 
3. 

---

## 15. Final Development Checklist

- [ ] Design tokens defined
- [ ] Components identified
- [ ] Pages/screens structured
- [ ] Responsive rules documented
- [ ] Interaction states defined
- [ ] Form states defined
- [ ] Accessibility notes included
- [ ] Content gaps listed
- [ ] Assets listed
- [ ] CMS requirements documented
- [ ] Performance risks reviewed
- [ ] Implementation risks listed
- [ ] Open questions documented

---

## 16. Final Recommendation

**Handoff Status:** Ready / Ready With Notes / Needs Clarification / Not Ready  

**Reason:**  
```

---

## Component Documentation Format

When documenting an important component in detail, use this format:

```md
## Component: [Component Name]

**Purpose:**  
**Used On:**  
**Variants:**  

**Anatomy:**  
- 
- 
- 

**States:**  
- Default:
- Hover:
- Focus:
- Active:
- Disabled:
- Loading:
- Error:
- Success:

**Responsive Behavior:**  
- Desktop:
- Tablet:
- Mobile:

**Accessibility Notes:**  
- 
- 

**Developer Notes:**  
- 
- 
```

---

## Common Developer Rules By Project Type

### Landing Page

Common rules:

```md
- Keep primary CTA visible in hero and repeat after proof sections.
- Collapse 3-column sections into 1 column below 768px.
- Use real form labels, not placeholder-only labels.
- Add success and error states for consultation/contact form.
- Optimize all hero and project images for performance.
```

### SaaS Dashboard

Common rules:

```md
- Collapse sidebar into drawer below 1024px.
- Convert data tables into mobile cards below 768px.
- Add skeleton loading states for metrics and tables.
- Define empty states for no data and no search results.
- Keep primary actions visible in the top area.
```

### Admin Panel

Common rules:

```md
- Add confirmation modal for destructive actions.
- Keep filters persistent or accessible via drawer on mobile.
- Use status badges with text labels, not color alone.
- Provide empty, loading, and error states for all lists.
```

### Ecommerce

Common rules:

```md
- Keep product price and add-to-cart visible.
- Convert filters into a drawer on mobile.
- Add product image fallback.
- Define out-of-stock and sale states.
- Use sticky add-to-cart on mobile product detail pages.
```

### Mobile App

Common rules:

```md
- Keep primary actions within thumb reach.
- Use bottom navigation for core sections.
- Avoid dense tables on mobile.
- Minimize typing with selects, chips, or defaults.
```

---

## Quality Checklist

Before finalizing the Developer Handoff Document, check:

- [ ] Is the project summary clear?
- [ ] Is final design direction documented?
- [ ] Are design tokens included?
- [ ] Are components listed?
- [ ] Are component states included?
- [ ] Are page/screen structures included?
- [ ] Are responsive rules specific?
- [ ] Are interaction states documented?
- [ ] Are animation notes included?
- [ ] Are accessibility notes included?
- [ ] Are content and asset gaps listed?
- [ ] Are CMS/dynamic content notes included if needed?
- [ ] Are performance notes included?
- [ ] Are implementation risks included?
- [ ] Are developer questions listed?
- [ ] Is handoff status clear?

---

## Anti-Patterns To Avoid

Do not:

- Give vague developer instructions.
- Skip states.
- Skip responsive behavior.
- Skip accessibility notes.
- Skip content gaps.
- Ignore CMS/dynamic content needs.
- Ignore performance impact of images/videos.
- Ignore mobile navigation behavior.
- Assume developers can infer complex interactions.
- Provide only aesthetic notes.
- Leave component variants undefined.
- Mark handoff ready if major information is missing.

---

## Example Trigger Phrases

Use this skill when the user says:

- “Create developer handoff.”
- “Prepare handoff notes.”
- “Make this ready for development.”
- “Convert this UI into developer instructions.”
- “Create implementation notes.”
- “Document components and tokens.”
- “Prepare frontend handoff.”
- “What should I give to developers?”
- “Create dev-ready UI documentation.”
- “Generate design handoff.”

---

## Example Lightweight Output

```md
# Developer Handoff Document

## 1. Project Summary

**Client/Product:** UrbanNest Interiors  
**Project Type:** Premium interior design landing page  
**Platform/Framework:** Next.js assumed  
**CMS Requirement:** Optional CMS for projects/testimonials  
**Primary User Action:** Book a consultation  
**Primary Business Goal:** Generate qualified consultation leads  
**Final Design Status:** Approved with responsive notes  

---

## 2. Final Design Direction

**Visual Style:** Quiet luxury editorial  
**Brand Feel:** Premium, calm, warm, refined  
**UX Approach:** Conversion-focused landing page with early proof and consultation CTA  
**Layout Style:** Desktop-first responsive, spacious, image-led sections  
**Component Style:** Minimal cards, thin borders, soft surfaces, restrained shadows  
**Motion Style:** Subtle reveals, refined hover states, no bouncy effects  
**Accessibility Priority:** Readable text, visible focus states, usable forms  

---

## 6. Responsive Rules

### Desktop

- Use max-width container of 1200px.
- Use spacious section padding of 80–96px.
- Hero may use two-column layout with text and imagery.
- Project showcase can use asymmetrical grid.

### Tablet

- Reduce section spacing to 56–72px.
- Collapse large asymmetrical grids into simpler two-column layouts.
- Keep CTA visible after hero intro.

### Mobile

- Use 16px horizontal padding.
- Stack hero text first, CTA second, trust proof third, image fourth.
- Collapse all multi-column sections into one column.
- Keep consultation CTA visible early.
- Use full-width buttons for primary actions.
- Keep form fields full width.

---

## 13. Implementation Risks

- Missing premium photography may reduce final design quality.
- Long client copy may break section rhythm.
- Heavy image use may affect performance if not optimized.
- CMS project cards need content length limits.

---

## 16. Final Recommendation

**Handoff Status:** Ready With Notes  

**Reason:** The design direction is stable and buildable, but final imagery, copy, and form validation states must be confirmed before development.
```

---

## Project Memory Behavior

**Skill Number:** 08
**Skill Role:** Developer Handoff — final skill, converts approved design into implementation-ready documentation.

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
- `.agency/DESIGN_DNA.md`
- `.agency/RESPONSIVE_ACCESSIBILITY_REVIEW.md`

### Skill Output Files

After completing this skill, write output to:

- `.agency/DEVELOPER_HANDOFF.md` — the Developer Handoff Document
- `.agency/PROJECT_STATE.json` — updated state (mark phase as handoff-complete)
- `.agency/CURRENT_CONTEXT.md` — updated session context
- `.agency/CONTEXT_INDEX.json` — updated index
- `.agency/CHANGELOG.md` — append entry
- `.agency/TODO.md` — update with any remaining open questions

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

1. Save the Developer Handoff Document to `.agency/DEVELOPER_HANDOFF.md`.
2. Update `.agency/CURRENT_CONTEXT.md` with current phase as `handoff-complete`.
3. Update `.agency/PROJECT_STATE.json` — mark `handoff_complete: true`.
4. Update `.agency/CONTEXT_INDEX.json`:
   - Set `current_phase` to `handoff-complete`
   - Set `current_skill` to `development`
   - Set `required_context_files` to `[".agency/CURRENT_CONTEXT.md", ".agency/DEVELOPER_HANDOFF.md", ".agency/DESIGN_DNA.md"]`
5. Append a final project entry to `.agency/CHANGELOG.md`.
6. Update `.agency/TODO.md` with any open questions for developers.
7. Add final implementation decisions to `.agency/DECISIONS.md`.
8. Do not delete previous decisions or changelog entries.
