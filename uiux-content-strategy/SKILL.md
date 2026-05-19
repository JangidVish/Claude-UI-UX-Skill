---
skill_id: uiux-content-strategy
skill_number: 06.5
requires_visual_input: false
requires_browser: false
project_complexity: standard, full
human_checkpoint_after: false
output_file: .agency/CONTENT_STRATEGY.md
reads_from:
  - .agency/CLIENT_BRIEF.md
  - .agency/UX_STRATEGY.md
  - .agency/DESIGN_DNA.md
  - .agency/WIREFRAMES.md
---

# Content Strategy Skill

## Purpose

This skill generates the actual copy for every section of the UI.

Not placeholder copy. Not lorem ipsum. Real headlines, CTAs, section headings, body text, microcopy, form labels, error messages, and SEO meta content — all derived from the project brief, UX strategy, and Design DNA.

Use this skill after Design DNA is complete. Before UI generation, so the generation prompt uses real copy. Or before developer handoff, so the developer has final content to implement.

---

## When To Use

- After Design DNA is complete
- Before generating the UI prompt (so Stitch/V0/Framer get real copy)
- Before developer handoff (so final content is documented)
- When client needs to review and approve copy before build
- When a copywriter has not been assigned to the project

Skip for lite projects if the client is providing their own copy. Mark in `PROJECT_STATE.json` as `skipped`.

---

## Core Behavior

When triggered, act as a senior UX copywriter who understands conversion design, brand voice, and UI writing principles.

Your job:

1. Read CLIENT_BRIEF.md for business, audience, goals, CTAs, and brand personality.
2. Read UX_STRATEGY.md for page hierarchy, user journey, and conversion flow.
3. Read DESIGN_DNA.md for tone, personality words, and words to avoid.
4. Read WIREFRAMES.md for section structure and content slots (if available).
5. Generate copy for every required page and section in the project.
6. Validate copy against brand direction and conversion goals before outputting.

---

## Copy Quality Rules

### 1. Every Headline Must Pass The "So What?" Test

Weak: "Welcome to UrbanNest Interiors"
Strong: "Your Home, Designed to Match the Life You Actually Live"

Weak: "Our Services"
Strong: "From First Sketch to Final Reveal — We Handle Everything"

### 2. CTAs Must State What Happens Next

Weak: "Submit", "Get Started", "Learn More"
Strong: "Book Your Free Consultation", "See How It Works", "Get My Custom Quote"

### 3. Body Copy Must Speak To The User's Pain, Not The Company's Features

Weak: "We have 10 years of experience and a team of experts."
Strong: "You've redesigned in your head a hundred times. We make it actually happen — on time, on budget, no surprises."

### 4. Match Tone To Brand Personality

Read `DESIGN_DNA.md` → Brand Personality section. Apply matching language.

| Brand Personality | Copy Tone |
|---|---|
| Premium / Luxury | Confident, sparse, no exclamation marks |
| Friendly / Warm | Conversational, second person, light humor |
| Bold / Energetic | Short sentences, active verbs, punchy |
| Corporate / Enterprise | Professional, clear, trust-focused |
| Minimal / Calm | Simple, honest, whitespace in language too |
| Futuristic / Technical | Precise, forward-looking, intelligent |

### 5. Microcopy Matters

Every input field label, placeholder, error message, success message, empty state, and tooltip must be written. These are the moments that reduce friction or increase abandonment.

### 6. Never Write Buzzwords

Never use:
- "world-class"
- "innovative solutions"
- "cutting-edge"
- "leverage"
- "synergy"
- "best-in-class"
- "game-changing"
- "seamless"
- "robust"
- "holistic"

If a line sounds like it could appear on any competitor's site, rewrite it.

---

## SEO Copy Requirements

For every page, generate:

- `<title>` tag (50–60 characters)
- Meta description (140–160 characters)
- H1 (primary keyword focus, matches hero headline)
- Suggested URL slug

Do not stuff keywords. Write for humans first, search engines second.

---

## Output Format

Write the output section by section, page by page.

```md
# Content Strategy

## Project Copy Summary

**Brand Voice:** [2–3 words]
**Tone Benchmark:** [brands whose copy tone to reference]
**Words To Use:** [from Design DNA]
**Words To Avoid:** [from Design DNA + buzz word list]
**Primary CTA Phrase:** [final decided CTA]
**Secondary CTA Phrase:** [final decided secondary CTA]

---

## Page: [Page Name]

### SEO

**Title Tag:** [50–60 chars]
**Meta Description:** [140–160 chars]
**H1:** [headline]
**URL Slug:** /[slug]

---

### Section: [Section Name]

**Section Role:** [what this section does in the conversion flow]

**Headline:**
[Headline text]

**Subheadline / Supporting Line:**
[Supporting line]

**Body Copy:**
[Body text — 1–4 sentences max per block]

**CTA:**
[CTA label + destination]

**Trust Signal / Social Proof:**
[Stat, quote, or badge text if applicable]

**Microcopy:**
[Any small supporting text — under CTA, near form, helper text]

---
```

Repeat the Section block for every section in the wireframe or UX strategy.

---

## Required Sections Per Project Type

### Landing Page (Lite)

- Hero
- Problem / Pain Point
- Solution / Offer
- How It Works
- Social Proof / Testimonials
- CTA Block
- FAQ
- Footer

### Multi-Page Website (Standard)

- Homepage: Hero, Features, How It Works, Testimonials, CTA
- About: Mission, Team, Values, CTA
- Services: Service cards, Process, CTA
- Contact: Form copy, labels, confirmation message

### SaaS Product

- Hero
- Problem Statement
- Feature Sections (one per core feature)
- Pricing: Plan names, plan descriptions, feature labels, CTA per plan
- Onboarding Microcopy: Empty states, tooltips, placeholder text, error messages
- Dashboard copy if applicable

---

## Form Copy Requirements

For every form in the project, generate:

| Element | What To Write |
|---|---|
| Form heading | What the user gets from completing this |
| Input labels | Clear, not generic |
| Placeholder text | Helpful example, not label repeat |
| Submit button | Specific action ("Send My Inquiry") |
| Success message | Confirm what happens next ("We'll reply within 24 hours") |
| Error messages | Human, specific ("Phone number must be 10 digits") |
| Privacy note | Short trust line near form |

---

## Validation Before Output

Before writing the final output, check:

- [ ] Every headline is specific, not generic
- [ ] Every CTA tells the user what happens next
- [ ] No buzzwords used
- [ ] Copy matches brand personality from Design DNA
- [ ] All form fields and microcopy are written
- [ ] SEO titles and descriptions are within character limits
- [ ] Conversion flow copy matches UX strategy journey
- [ ] Copy speaks to user pain points, not company features

---

## Example Output Fragment

```md
## Page: Homepage

### SEO

**Title Tag:** Premium Interior Design in Mumbai | UrbanNest Interiors
**Meta Description:** UrbanNest transforms homes into spaces that feel completely yours. Book a free consultation with our design team today.
**H1:** Your Home, Designed to Match the Life You Actually Live
**URL Slug:** /

---

### Section: Hero

**Section Role:** First impression — capture attention, communicate core benefit, drive booking CTA

**Headline:**
Your Home, Designed to Match the Life You Actually Live

**Subheadline:**
Premium residential interiors in Mumbai. Turnkey execution. No surprises.

**Body Copy:**
You know what you want. You just haven't found someone who can make it real. We've delivered 200+ projects, and we still treat every room like it's our first one.

**CTA:**
Book a Free Consultation → [/contact]

**Trust Signal:**
200+ Homes Completed · Avg. 4.9★ on Google

**Microcopy:**
Free consultation. No commitment required.

---

### Section: How It Works

**Section Role:** Reduce uncertainty — show process so user trusts the execution

**Headline:**
From First Conversation to Final Reveal

**Step 1:**
Label: Discovery Call
Copy: Tell us about your space. We ask questions. We listen.

**Step 2:**
Label: Design Proposal
Copy: You receive a full concept — materials, furniture, layout — before we start.

**Step 3:**
Label: Execution
Copy: We manage vendors, timelines, and quality. You just wait for the reveal.

**CTA:**
Start With a Free Call → [/contact]
```

---

## Project Memory Behavior

**Skill Number:** 06.5
**Reads from:** `.agency/CLIENT_BRIEF.md`, `.agency/UX_STRATEGY.md`, `.agency/DESIGN_DNA.md`, `.agency/WIREFRAMES.md`
**Writes to:** `.agency/CONTENT_STRATEGY.md`

Before running:

1. Check `.agency/` exists.
2. Read `.agency/CURRENT_CONTEXT.md`.
3. Read `.agency/CONTEXT_INDEX.json`.
4. Read required files: `CLIENT_BRIEF.md`, `UX_STRATEGY.md`, `DESIGN_DNA.md`.
5. Read `WIREFRAMES.md` if it exists.
6. Do not read files not listed above.

---

## Session Resume Behavior

1. Do not ask the user to repeat project context.
2. Read `.agency/CURRENT_CONTEXT.md`.
3. Read `.agency/CONTEXT_INDEX.json`.
4. Read `CLIENT_BRIEF.md`, `UX_STRATEGY.md`, `DESIGN_DNA.md`.
5. Summarize: project name, industry, target audience, brand voice, pages to write copy for.
6. Continue from where copy left off — do not restart if partial copy exists.

---

## Post-Task Update Behavior

After completing this skill:

1. Save all copy to `.agency/CONTENT_STRATEGY.md`.
2. Update `.agency/CURRENT_CONTEXT.md`:
   - Set current phase to `content-strategy`
   - Mark content-strategy as completed
3. Update `.agency/PROJECT_STATE.json`:
   - Set `content_strategy.status` to `complete`
   - Set `content_strategy.completed_at` to today's date
4. Update `.agency/CONTEXT_INDEX.json`:
   - Set `current_skill` to `responsive-review` or `ui-generation-prompt`
   - Add `content_strategy` to `required_context_files` for downstream skills
5. Append entry to `.agency/CHANGELOG.md`.
6. Update `.agency/TODO.md`.
7. Add key copy decisions (brand voice direction, CTA wording) to `.agency/DECISIONS.md`.
8. Do not delete previous content.

---

## Example Trigger Phrases

- "Write the copy for this project."
- "Generate content strategy."
- "Write headlines and CTAs."
- "I need copy for the landing page."
- "Generate the page copy before Stitch."
- "Write the form microcopy."
- "Create SEO copy for all pages."
