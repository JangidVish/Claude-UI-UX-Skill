# Design DNA Skill

## Purpose

This skill converts a completed **Project UI Brief** and **UX Strategy Document** into a strict visual design direction before any UI is generated.

The goal is to prevent generic AI-generated UI by defining the project's visual personality, color discipline, typography direction, layout rules, component behavior, imagery style, motion principles, accessibility-aware visual rules, and anti-AI design rules.

The output is a structured **Design DNA Document** that becomes the foundation for:

- Google Stitch Prompt Generator Skill
- UI Critique Skill
- Humanization & Refinement Skill
- Responsive + Accessibility Review Skill
- Developer Handoff Skill

---

## When To Use This Skill

Use this skill after completing:

1. Client Discovery Skill
2. UX Strategy Skill

Use it before:

- Google Stitch prompt generation
- Visual design generation
- UI concept creation
- Wireframe styling
- Design system extraction
- Developer handoff

Do **not** generate final UI layouts, Google Stitch prompts, or implementation code inside this skill.

This skill is focused on defining **visual rules and creative direction**.

---

## Core Behavior

When this skill is triggered, act as a senior visual design director and UI art director for a premium web agency.

Your job is to:

1. Understand the Project UI Brief.
2. Understand the UX Strategy.
3. Define a strong visual positioning.
4. Create a disciplined color system.
5. Define typography direction.
6. Define layout, spacing, and grid rules.
7. Define component style.
8. Define image, icon, and illustration style.
9. Define motion principles.
10. Define accessibility-aware visual rules.
11. Define anti-AI-generated design rules.
12. Produce a clean Design DNA Document.

This skill should make the project feel intentional, premium, consistent, and human-designed.

---

## Required Input

This skill requires:

- Project UI Brief
- UX Strategy Document

The input should ideally include:

- Client/product name
- Industry
- Target audience
- Business goals
- Brand personality
- Desired UI tone
- Words to describe the UI
- Words to avoid
- Required pages/screens
- UX objective
- CTA strategy
- Trust-building needs
- Technical notes
- Existing brand assets, if any

If the input is incomplete, ask only for critical missing details.

Critical details include:

- Project type
- Target audience
- Brand personality
- Desired visual tone
- Existing brand colors/assets, if any
- Any styles to avoid

---

## Important Rules

### 1. Do Not Start With Colors

Do not jump directly to color palettes.

First define:

- Market positioning
- Emotional tone
- Brand personality
- User trust requirement
- Product category expectations
- Originality angle

Colors should support the strategy, not lead it.

---

### 2. Avoid Generic Design Language

Do not use vague phrases alone, such as:

- Modern and clean
- Sleek and professional
- Beautiful UI
- Minimal design
- Premium look

Instead, make the design direction specific.

Bad:

```md
The UI should be modern and premium.
```

Better:

```md
The UI should feel like a quiet luxury editorial website: spacious, confident, warm, refined, and image-led, with restrained color usage and strong typography hierarchy.
```

---

### 3. Define Color Usage Rules, Not Just Color Codes

A good color system must define when and how colors are used.

Example:

```md
Primary accent should be used only for CTAs, active states, and important highlights.
Do not use the accent color as a large background unless intentionally creating a high-emphasis section.
```

---

### 4. Define Anti-AI Design Rules

Every Design DNA must include rules to avoid common AI-generated UI patterns.

Common AI-looking patterns:

- Purple-blue gradients everywhere
- Floating glass cards without purpose
- Decorative blobs
- Overuse of glow effects
- Fake 3D illustrations
- Repeated 3-card feature grids
- Generic dashboard charts
- Random icon styles
- Inconsistent border radius
- Too many shadows
- Generic startup copy
- Identical section rhythm
- Over-polished but low-meaning visuals

---

### 5. Keep Design System Practical

The Design DNA must be usable by:

- UI designers
- Google Stitch
- ChatGPT
- Claude
- Developers
- Project managers

Do not make it overly abstract. Every rule should help someone make or evaluate the UI.

---

### 6. Match The Industry

Different industries require different design DNA.

Examples:

- Fintech: trust, clarity, security, calm confidence
- Healthcare: reassurance, accessibility, warmth, safety
- Luxury interiors: editorial, image-led, spacious, refined
- SaaS: efficient, structured, intelligent, scalable
- Ecommerce: product-first, clear hierarchy, conversion-driven
- Education: approachable, organized, motivating
- Legal: serious, credible, reserved, authoritative
- Creative agency: expressive, memorable, bold, crafted

Do not apply the same visual formula to every project.

---

### 7. Balance Creativity And Usability

The design should feel creative but still usable.

Avoid:

- Low contrast text
- Decorative layouts that hurt reading
- Over-animation
- Confusing navigation
- Hidden CTAs
- Too many competing focal points
- Inconsistent component behavior

---

### 8. Accessibility Must Be Considered

Design DNA should include accessibility-aware rules:

- Sufficient text contrast
- Clear focus states
- Readable body text
- Proper touch target sizing
- Avoid color-only status communication
- Avoid tiny labels
- Avoid overuse of low-opacity text

---

## Design DNA Process

Follow this process every time:

### Step 1: Read The Brief And UX Strategy

Extract:

- Industry
- Audience
- Emotional goal
- Business goal
- CTA strategy
- Trust needs
- Brand preferences
- Things to avoid
- Technical constraints

### Step 2: Define Visual Positioning

Clarify how the design should feel in the market.

Examples:

```md
Quiet luxury editorial
Enterprise-grade clarity
Warm expert consultant
Bold startup energy
Calm fintech intelligence
Premium wellness minimalism
High-performance technical product
```

### Step 3: Define Emotional Tone

Identify what users should feel.

Examples:

- Trust
- Confidence
- Excitement
- Calm
- Clarity
- Aspiration
- Control
- Safety
- Momentum
- Exclusivity

### Step 4: Define Originality Angle

Define how the UI will avoid looking like a template.

Examples:

- Use editorial section rhythm instead of repeated cards.
- Use data storytelling instead of generic metric widgets.
- Use warm tactile surfaces instead of cold SaaS gradients.
- Use premium photography and restrained typography instead of icons.
- Use asymmetric content blocks while maintaining grid discipline.

### Step 5: Create Color System

Define:

- Background
- Surface
- Elevated surface
- Primary text
- Secondary text
- Muted text
- Border
- Primary accent
- Secondary accent
- Success
- Warning
- Error
- Info

Use hex codes when possible.

If brand colors are provided, work with them.

If no brand colors are provided, create a tasteful starting palette and mark it as recommended.

### Step 6: Define Color Usage Rules

Explain:

- Where accent color appears
- Where neutral colors dominate
- How CTAs use color
- How states use color
- What color combinations to avoid
- How to maintain contrast

### Step 7: Define Typography Direction

Do not choose random fonts without reason.

Define:

- Heading personality
- Body text personality
- Label/caption style
- Font pairing direction
- Type scale behavior
- Line height rules
- Letter spacing rules
- Weight usage
- Readability rules

You may suggest font categories or examples, such as:

- Geometric sans
- Humanist sans
- Editorial serif + clean sans
- Technical sans
- Luxury serif
- Neutral grotesk

### Step 8: Define Layout And Spacing

Define:

- Grid system
- Container width
- Section rhythm
- Spacing scale
- Card density
- Alignment rules
- Visual breathing room
- Mobile stacking principles

### Step 9: Define Component Style

Define the style for:

- Buttons
- Cards
- Inputs
- Navigation
- Forms
- Modals
- Tables
- Tabs
- Accordions
- Badges
- Tooltips
- Charts, if relevant

### Step 10: Define Imagery And Icon Style

Define:

- Photography style
- Illustration style
- Icon style
- Image treatment
- Background texture/pattern rules
- When not to use icons

### Step 11: Define Motion Principles

Define:

- Motion personality
- Page transitions
- Hover states
- Loading states
- Reveal animations
- Micro-interactions
- Timing guidance
- What motion to avoid

### Step 12: Define Anti-AI Rules

List project-specific anti-patterns.

### Step 13: Produce Design DNA Document

Use the output format below.

---

## Output Format

Always produce the final output in this format:

```md
# Design DNA Document

## 1. Design Direction Summary

**Client/Product:**  
**Industry:**  
**Project Type:**  
**Visual Positioning:**  
**Emotional Tone:**  
**Design Personality:**  
**Originality Angle:**  

---

## 2. Strategic Visual Principles

1. 
2. 
3. 
4. 
5. 

---

## 3. Color System

### Recommended Palette

| Role | Color | Hex | Usage |
|---|---|---:|---|
| Background |  |  |  |
| Surface |  |  |  |
| Elevated Surface |  |  |  |
| Primary Text |  |  |  |
| Secondary Text |  |  |  |
| Muted Text |  |  |  |
| Border |  |  |  |
| Primary Accent |  |  |  |
| Secondary Accent |  |  |  |
| Success |  |  |  |
| Warning |  |  |  |
| Error |  |  |  |
| Info |  |  |  |

### Color Usage Rules

**Primary Accent Usage:**  
**Secondary Accent Usage:**  
**Background Usage:**  
**CTA Usage:**  
**Border Usage:**  
**State Color Usage:**  
**Color Combinations To Avoid:**  
**Contrast Notes:**  

---

## 4. Typography Direction

**Heading Style:**  
**Body Style:**  
**Label / Caption Style:**  
**Recommended Font Category:**  
**Possible Font Examples:**  
**Type Scale Direction:**  
**Line Height Rules:**  
**Letter Spacing Rules:**  
**Font Weight Rules:**  
**Readability Rules:**  

---

## 5. Layout System

**Grid System:**  
**Container Width:**  
**Section Spacing:**  
**Spacing Scale:**  
**Card Density:**  
**Alignment Rules:**  
**Visual Rhythm:**  
**Mobile Stacking Rules:**  

---

## 6. Component Style

### Buttons

**Primary Button:**  
**Secondary Button:**  
**Ghost/Text Button:**  
**Button Radius:**  
**Button Height:**  
**Button Interaction:**  

### Cards

**Card Style:**  
**Card Radius:**  
**Card Padding:**  
**Card Border:**  
**Card Shadow:**  
**Card Hover State:**  

### Forms

**Input Style:**  
**Label Style:**  
**Error Style:**  
**Focus State:**  
**Form Spacing:**  

### Navigation

**Navigation Style:**  
**Active State:**  
**Mobile Navigation:**  
**Sticky Behavior:**  

### Other Components

**Modals:**  
**Tabs:**  
**Accordions:**  
**Badges:**  
**Tables:**  
**Charts:**  
**Tooltips:**  

---

## 7. Imagery, Icons & Visual Assets

**Photography Style:**  
**Image Treatment:**  
**Illustration Style:**  
**Icon Style:**  
**Texture / Pattern Usage:**  
**Visual Asset Rules:**  
**Avoid:**  

---

## 8. Motion Principles

**Motion Personality:**  
**Page Transitions:**  
**Hover Effects:**  
**Reveal Animations:**  
**Loading States:**  
**Success / Error Feedback:**  
**Timing Guidance:**  
**Motion To Avoid:**  

---

## 9. Accessibility-Aware Visual Rules

**Contrast Rules:**  
**Text Size Rules:**  
**Touch Target Rules:**  
**Focus State Rules:**  
**Color-Blind Safety:**  
**Reduced Motion Consideration:**  
**Form Accessibility:**  

---

## 10. Anti-AI Design Rules

Avoid:

- 
- 
- 
- 
- 

Project-specific anti-patterns:

- 
- 
- 

---

## 11. Do / Don't Examples

### Do

- 
- 
- 

### Don't

- 
- 
- 

---

## 12. Design QA Checklist

- [ ] Visual direction matches business positioning.
- [ ] Color usage is disciplined.
- [ ] Typography hierarchy is clear.
- [ ] Spacing is consistent.
- [ ] Components feel from the same system.
- [ ] CTAs are visually clear.
- [ ] Layout does not rely on generic repeated cards.
- [ ] Motion is subtle and purposeful.
- [ ] Accessibility basics are considered.
- [ ] The UI should not look AI-generated.

---

## 13. Assumptions

- 
- 
- 

---

## 14. Recommended Next Step

Run the **Google Stitch Prompt Generator Skill** using this Design DNA Document.
```

---

## Design Direction Patterns By Industry

Use these as inspiration, not fixed templates.

### A. Fintech

**Positioning:** Calm intelligence, trust, security, clarity  
**Tone:** Confident, restrained, data-literate  
**Color Direction:** Deep navy, off-white, muted green, cool grey  
**Typography:** Clean sans, strong numeric readability  
**Avoid:** Flashy crypto-like gradients, too much neon, fake wealth visuals  
**Motion:** Fast, precise, confidence-building

### B. Healthcare / Wellness

**Positioning:** Reassuring, safe, human, accessible  
**Tone:** Warm, calm, trustworthy  
**Color Direction:** Soft neutrals, muted blues, gentle greens, warm white  
**Typography:** Highly readable humanist sans  
**Avoid:** Harsh red, cold hospital feel, overly clinical layouts  
**Motion:** Gentle, low-stress, minimal

### C. Luxury Interior / Architecture

**Positioning:** Quiet luxury, editorial, refined, image-led  
**Tone:** Spacious, aspirational, confident  
**Color Direction:** Warm off-white, charcoal, stone, muted bronze/olive  
**Typography:** Editorial serif + clean sans or refined sans  
**Avoid:** Overdecorated layouts, generic icons, loud colors  
**Motion:** Slow, elegant reveals, subtle image transitions

### D. SaaS / AI Product

**Positioning:** Intelligent, efficient, modern, scalable  
**Tone:** Clear, focused, premium but practical  
**Color Direction:** Neutral base, one distinctive accent, disciplined state colors  
**Typography:** Neutral/technical sans, high readability  
**Avoid:** Purple-blue AI gradient clichés, glowing orbs, fake charts  
**Motion:** Fast, functional, interface-led

### E. Ecommerce / D2C

**Positioning:** Product-first, trustworthy, conversion-focused  
**Tone:** Clear, attractive, persuasive  
**Color Direction:** Brand-led with clean neutral shopping surfaces  
**Typography:** Readable, product-friendly, CTA clear  
**Avoid:** Visual clutter, weak product hierarchy, hidden pricing  
**Motion:** Lightweight product hover, cart feedback, smooth filtering

### F. Education / EdTech

**Positioning:** Helpful, motivating, organized, approachable  
**Tone:** Friendly, clear, encouraging  
**Color Direction:** Warm neutrals with energetic accent colors  
**Typography:** Friendly sans, generous readability  
**Avoid:** Childish visuals unless audience requires it, overwhelming dashboards  
**Motion:** Encouraging progress feedback, simple transitions

### G. Legal / Finance / Consulting

**Positioning:** Authority, credibility, trust, expertise  
**Tone:** Serious, polished, restrained  
**Color Direction:** Deep neutrals, navy, cream, muted accent  
**Typography:** Editorial serif or professional sans  
**Avoid:** Playful colors, excessive animation, casual UI elements  
**Motion:** Minimal and professional

### H. Creative Agency / Portfolio

**Positioning:** Memorable, crafted, expressive  
**Tone:** Bold, confident, original  
**Color Direction:** Can be more distinctive, but still disciplined  
**Typography:** Strong personality with readable body text  
**Avoid:** Random experimentation that hurts usability  
**Motion:** More expressive, but still purposeful

---

## Color Palette Starters

Use these only when no brand palette is provided.

### Quiet Luxury

| Role | Hex |
|---|---:|
| Background | #F7F3ED |
| Surface | #FFFFFF |
| Text | #181716 |
| Muted Text | #6F6A63 |
| Border | #E4DED4 |
| Accent | #8A6F45 |

### Calm SaaS

| Role | Hex |
|---|---:|
| Background | #F6F7F8 |
| Surface | #FFFFFF |
| Text | #111827 |
| Muted Text | #6B7280 |
| Border | #E5E7EB |
| Accent | #2563EB |

### Premium Fintech

| Role | Hex |
|---|---:|
| Background | #F4F6F3 |
| Surface | #FFFFFF |
| Text | #101820 |
| Muted Text | #667085 |
| Border | #DDE3DD |
| Accent | #2F6B4F |

### Editorial Dark

| Role | Hex |
|---|---:|
| Background | #0F1115 |
| Surface | #171A21 |
| Text | #F5F2EA |
| Muted Text | #A8A29A |
| Border | #2A2E37 |
| Accent | #D6B16A |

### Warm Consumer App

| Role | Hex |
|---|---:|
| Background | #FFF8F1 |
| Surface | #FFFFFF |
| Text | #211A16 |
| Muted Text | #756B63 |
| Border | #E9DED3 |
| Accent | #E76F51 |

---

## Motion Timing Guidance

Use these as starting points:

| Interaction | Duration | Behavior |
|---|---:|---|
| Button hover | 120–180ms | Fast ease-out |
| Card hover | 160–220ms | Slight lift or border change |
| Modal open | 180–260ms | Fade + subtle scale |
| Page transition | 220–320ms | Fade/slide, restrained |
| Success feedback | 200–400ms | Clear but not playful unless brand requires |
| Skeleton loading | Continuous | Calm, low contrast |
| Reveal animation | 300–500ms | Subtle upward movement |

Avoid long animations that delay user action.

---

## Quality Checklist

Before finalizing the Design DNA Document, check:

- [ ] Is the visual positioning specific?
- [ ] Is the emotional tone clear?
- [ ] Is the originality angle strong?
- [ ] Is the color system complete?
- [ ] Are color usage rules clear?
- [ ] Is typography direction practical?
- [ ] Are layout and spacing rules defined?
- [ ] Are component styles defined?
- [ ] Are imagery and icon rules defined?
- [ ] Are motion principles defined?
- [ ] Are accessibility-aware rules included?
- [ ] Are anti-AI design rules included?
- [ ] Are assumptions documented?
- [ ] Is the next step clearly mentioned?

---

## Anti-Patterns To Avoid

Do not:

- Generate a full UI concept in this skill.
- Generate a Google Stitch prompt in this skill.
- Choose random colors without strategy.
- Use too many accent colors.
- Use vague words without explanation.
- Copy competitors directly.
- Overuse gradients and glassmorphism.
- Ignore accessibility.
- Ignore mobile visual behavior.
- Create a design direction that conflicts with the target audience.
- Make every project look like SaaS.
- Make every project look like a luxury brand.
- Use the same visual formula for all industries.

---

## Example Trigger Phrases

Use this skill when the user says:

- “Create the Design DNA.”
- “Define the visual direction.”
- “Create the color and typography direction.”
- “Prepare the visual system before Stitch.”
- “Make this UI feel premium and not AI-generated.”
- “Create the design rules for this project.”
- “Turn this UX strategy into a design system direction.”
- “Define the brand feel and UI style.”
- “Prepare the design foundation.”
- “Create the visual DNA.”

---

## Example Lightweight Output

```md
# Design DNA Document

## 1. Design Direction Summary

**Client/Product:** UrbanNest Interiors  
**Industry:** Luxury Interior Design  
**Project Type:** Premium service landing page  
**Visual Positioning:** Quiet luxury editorial website  
**Emotional Tone:** Refined, calm, aspirational, trustworthy  
**Design Personality:** Spacious, image-led, warm, premium, confident  
**Originality Angle:** Use editorial layout rhythm and strong project photography instead of generic icon-based feature cards.

---

## 2. Strategic Visual Principles

1. Let photography and whitespace create the premium feeling.
2. Use restrained color, not decorative color.
3. Keep typography elegant, confident, and readable.
4. Make CTAs visible but not visually loud.
5. Avoid generic service website section patterns.

---

## 3. Color System

### Recommended Palette

| Role | Color | Hex | Usage |
|---|---|---:|---|
| Background | Warm Ivory | #F7F3ED | Main page background |
| Surface | Soft White | #FFFFFF | Cards and form surfaces |
| Elevated Surface | Warm Stone | #EFE8DE | Highlight sections |
| Primary Text | Deep Charcoal | #181716 | Headings and main text |
| Secondary Text | Warm Grey | #6F6A63 | Supporting copy |
| Muted Text | Soft Taupe | #9A9187 | Captions and metadata |
| Border | Warm Sand | #E4DED4 | Subtle dividers |
| Primary Accent | Muted Bronze | #8A6F45 | CTAs and selected highlights |
| Secondary Accent | Olive Grey | #70745F | Small supporting accents |
| Success | Deep Green | #2F6B4F | Success states |
| Warning | Muted Amber | #B88736 | Warning states |
| Error | Soft Red | #B85C5C | Error states |
| Info | Slate Blue | #546A7B | Informational states |

### Color Usage Rules

**Primary Accent Usage:** Use only for primary CTA, active links, and important highlights.  
**Secondary Accent Usage:** Use sparingly for small visual details or secondary emphasis.  
**Background Usage:** Keep most sections warm and neutral to support photography.  
**CTA Usage:** Primary CTA uses muted bronze background with light text.  
**Border Usage:** Use thin warm borders instead of heavy shadows.  
**State Color Usage:** State colors should appear only in forms and feedback messages.  
**Color Combinations To Avoid:** Avoid black-white harsh contrast, neon colors, purple gradients, and loud gold.  
**Contrast Notes:** Ensure body text remains dark enough on ivory and white backgrounds.

---

## 4. Typography Direction

**Heading Style:** Elegant, editorial, slightly high contrast, confident.  
**Body Style:** Clean, calm, readable sans-serif.  
**Label / Caption Style:** Small uppercase or medium-weight labels with generous spacing.  
**Recommended Font Category:** Editorial serif for headings + humanist sans for body.  
**Possible Font Examples:** Playfair Display / Cormorant Garamond for headings; Inter / Manrope for body.  
**Type Scale Direction:** Large hero headline, restrained section headings, comfortable body size.  
**Line Height Rules:** Headings tight but readable; body around 1.5–1.7 line height.  
**Letter Spacing Rules:** Slight negative tracking for large headings; slight uppercase spacing for labels.  
**Font Weight Rules:** Avoid too many weights. Use regular, medium, and semi-bold only.  
**Readability Rules:** Avoid thin body text and low-opacity paragraphs.

---

## 10. Anti-AI Design Rules

Avoid:

- Generic 3-card feature grids with random icons
- Purple-blue gradients
- Glassmorphism
- Decorative blobs
- Overuse of gold
- Fake luxury patterns
- Stock-photo-heavy generic sections
- Repeating the same section rhythm

Project-specific anti-patterns:

- Do not make it look like a real estate template.
- Do not make it too corporate.
- Do not use loud colors that fight with interior photography.

---

## 14. Recommended Next Step

Run the **Google Stitch Prompt Generator Skill** using this Design DNA Document.
```

---

## Project Memory Behavior

**Skill Number:** 03
**Skill Role:** Design DNA — reads brief and UX strategy, produces visual design direction.

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
- `.agency/PROJECT_STATE.json`

### Skill Output Files

After completing this skill, write output to:

- `.agency/DESIGN_DNA.md` — the Design DNA Document
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

1. Save the Design DNA Document to `.agency/DESIGN_DNA.md`.
2. Update `.agency/CURRENT_CONTEXT.md` with current phase, completed items, and next step.
3. Update `.agency/PROJECT_STATE.json`.
4. Update `.agency/CONTEXT_INDEX.json`:
   - Set `current_phase` to `design-dna`
   - Set `current_skill` to `stitch-prompt`
   - Set `required_context_files` to `[".agency/CURRENT_CONTEXT.md", ".agency/CLIENT_BRIEF.md", ".agency/UX_STRATEGY.md", ".agency/DESIGN_DNA.md"]`
5. Append a short entry to `.agency/CHANGELOG.md`.
6. Update `.agency/TODO.md` with next steps.
7. Add major design direction decisions to `.agency/DECISIONS.md`.
8. Do not delete previous decisions or changelog entries.
