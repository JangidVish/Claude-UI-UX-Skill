# Humanization & Refinement Skill

## Purpose

This skill converts a **UI Critique Report** into a clear, actionable refinement direction and Google Stitch refinement prompt.

The goal is to remove generic AI-generated patterns, strengthen visual hierarchy, improve brand alignment, increase content realism, and make the UI feel more custom, premium, and human-designed.

The output of this skill is a **Humanization & Refinement Plan** plus a ready-to-paste **Google Stitch Refinement Prompt**.

---

## When To Use This Skill

Use this skill after:

1. Google Stitch or another AI tool generates a UI concept.
2. UI Critique Skill has reviewed the concept.
3. The team wants to improve the design without starting from zero.

Use it for refining:

- Landing pages
- Corporate websites
- SaaS dashboards
- Admin panels
- Ecommerce pages
- Mobile app screens
- Web app screens
- Portfolio websites
- Booking platforms
- AI-generated UI screenshots
- Early Figma concepts
- Website builder outputs

Do **not** use this skill before a critique exists.

If no critique exists, first run the **UI Critique Skill**.

---

## Core Behavior

When this skill is triggered, act as a senior creative director, UI polish specialist, and AI-design humanization expert.

Your job is to:

1. Read the UI Critique Report.
2. Identify what should be preserved.
3. Identify what should be changed.
4. Identify what should be removed.
5. Convert weak areas into precise refinement instructions.
6. Remove AI-generated visual patterns.
7. Improve brand specificity.
8. Improve layout rhythm.
9. Improve copy realism.
10. Improve CTA hierarchy.
11. Maintain the existing Design DNA.
12. Produce a polished refinement prompt for Google Stitch.

This skill should not simply say “make it better.” It should tell exactly what to keep, fix, remove, and enhance.

---

## Required Input

This skill requires:

- UI Critique Report

Strongly recommended inputs:

- Original Google Stitch Prompt
- Project UI Brief
- UX Strategy Document
- Design DNA Document
- Screenshot or description of the current UI concept

If the Design DNA is missing, preserve the best existing direction and avoid introducing unrelated new visual styles.

---

## Important Rules

### 1. Preserve Before Changing

Do not regenerate everything unless the critique says the design is unusable.

First identify:

- What is working
- What should remain
- What visual direction is worth keeping
- Which components or sections are already strong

Example:

```md
Keep the warm neutral palette, strong hero spacing, and image-led direction.
```

---

### 2. Remove AI Smell Directly

Translate AI-smell issues into direct instructions.

Example critique:

```md
Repeated 3-card sections make it feel AI-generated.
```

Refinement instruction:

```md
Replace repeated 3-card feature sections with varied editorial layouts: one split feature section, one proof strip, and one process timeline.
```

---

### 3. Do Not Add Random Creativity

Humanization does not mean adding more decoration.

Avoid adding:

- Random gradients
- New colors
- Extra illustrations
- More shadows
- Heavy animation
- Unrelated design styles
- More sections without purpose

Humanization means making the design more intentional, contextual, and specific.

---

### 4. Maintain Design DNA

The refinement must respect the original Design DNA.

If the Design DNA says:

- Quiet luxury: keep refinement calm and restrained.
- Enterprise SaaS: keep refinement structured and efficient.
- Consumer app: keep refinement friendly and simple.
- Creative agency: refinement can be more expressive but still controlled.

Do not introduce a conflicting design style.

---

### 5. Improve Layout Rhythm

AI-generated UI often has repeated section patterns.

Improve rhythm with:

- Varied section compositions
- Different content densities
- Intentional contrast between sections
- Larger proof moments
- Better CTA pacing
- More natural transitions between sections

---

### 6. Improve Content Realism

Replace generic content with:

- Industry-specific labels
- Realistic metrics
- Specific user benefits
- Clear CTA text
- Believable testimonials
- Practical feature names
- Context-aware microcopy

Bad:

```txt
Feature One
Transform Your Business
Powerful Dashboard
```

Better:

```txt
Automated lead qualification
Book a site consultation
View renovation timeline
```

---

### 7. Improve CTA Hierarchy

Make sure there is:

- One dominant primary CTA
- One quieter secondary CTA
- Clear repeated CTA placement
- CTA after trust/proof moments
- Mobile CTA visibility

---

### 8. Improve Premium Feel By Reducing Noise

Premium often means:

- Better spacing
- Fewer visual tricks
- Stronger typography
- More restrained color
- Better imagery
- Clear hierarchy
- Consistent components
- Specific content

Not more decoration.

---

### 9. Create A Stitch-Ready Prompt

The final refinement prompt should be directly usable in Google Stitch.

It should include:

- Keep
- Improve
- Remove
- Layout changes
- Visual changes
- Content changes
- Motion changes
- Anti-AI rules
- Quality bar

---

## Refinement Process

Follow this process every time:

### Step 1: Read The Critique

Extract:

- Overall score
- Must-fix list
- AI-smell issues
- Weakest categories
- Strongest parts
- Keep/change/remove list
- Suggested refinement direction

### Step 2: Identify Preservation Rules

List what must remain consistent:

- Color palette
- Typography direction
- Layout strengths
- Brand tone
- Best sections
- Strong components

### Step 3: Identify Humanization Priorities

Choose the most important improvements.

Common priorities:

- Reduce generic AI look
- Improve visual hierarchy
- Improve content realism
- Improve section rhythm
- Improve CTA clarity
- Improve brand specificity
- Improve spacing discipline
- Improve component consistency

### Step 4: Define Layout Refinements

Specify changes such as:

- Move proof higher
- Replace repeated cards
- Use split layout
- Add comparison block
- Add process timeline
- Improve hero composition
- Simplify navigation
- Improve final CTA section

### Step 5: Define Visual Refinements

Specify changes such as:

- Reduce accent color
- Increase contrast
- Use consistent radius
- Simplify shadows
- Improve typography scale
- Improve image treatment
- Remove decorative effects

### Step 6: Define Content Refinements

Specify:

- Better headings
- More realistic labels
- Industry-specific copy
- Stronger CTA text
- Better microcopy
- More believable metrics/testimonials

### Step 7: Define Motion Refinements

Specify:

- Keep subtle animation
- Remove bouncy effects
- Use purposeful transitions
- Add loading/feedback if needed

### Step 8: Produce Final Output

Use the output format below.

---

## Output Format

Always produce the final output in this format:

```md
# Humanization & Refinement Plan

## 1. Refinement Objective

**Current UI Score:**  
**Primary Refinement Goal:**  
**Main Problem To Solve:**  
**Desired Result:**  

---

## 2. Preserve

Keep these parts of the current concept:

- 
- 
- 

---

## 3. Improve

Improve these areas:

- 
- 
- 

---

## 4. Remove / Reduce

Remove or reduce these AI-generated or weak elements:

- 
- 
- 

---

## 5. Layout Refinement Direction

- 
- 
- 

---

## 6. Visual Refinement Direction

- 
- 
- 

---

## 7. Content Refinement Direction

- 
- 
- 

---

## 8. Interaction / Motion Refinement Direction

- 
- 
- 

---

## 9. Humanization Rules

Make the next version feel more human-designed by:

- 
- 
- 
- 

---

## 10. Google Stitch Refinement Prompt

Copy and paste this prompt into Google Stitch:

---

Refine the previous UI concept.

## Keep

- 
- 
- 

## Improve

- 
- 
- 

## Remove / Avoid

- 
- 
- 

## Layout Changes

- 
- 
- 

## Visual Changes

- 
- 
- 

## Content Changes

- 
- 
- 

## Interaction & Motion Changes

- 
- 
- 

## Maintain Design System

Keep the same:
- Core color palette
- Typography direction
- Brand tone
- Button style
- Card radius
- Spacing discipline
- Navigation structure, unless listed as an issue

Do not introduce unrelated new styles.

## Anti-AI Rules

Avoid:
- Repeated 3-card layouts
- Generic placeholder content
- Decorative blobs
- Random gradients
- Unnecessary glassmorphism
- Fake dashboards or fake data
- Inconsistent shadows
- Inconsistent border radius
- Overuse of icons
- Same-height repetitive sections

## Final Quality Instruction

Make the UI feel more intentional, premium, brand-specific, conversion-focused, and human-crafted. The refined version should feel like it was improved by a senior UI/UX designer, not regenerated randomly.
```

---

## Refinement Modes

Use the correct mode based on critique score.

### Mode 1: Polish Only

Use when score is 8+.

Focus on:

- Microcopy
- Spacing
- Contrast
- CTA clarity
- Small component consistency
- Minor content improvements

Prompt phrase:

```txt
Do not restructure the full page. Keep the current layout and improve polish, hierarchy, content realism, and consistency.
```

---

### Mode 2: Moderate Refinement

Use when score is 6–7.9.

Focus on:

- Section rhythm
- CTA hierarchy
- Generic patterns
- Color discipline
- Better copy
- Stronger proof
- Improved component consistency

Prompt phrase:

```txt
Keep the strongest parts of the concept, but restructure weak sections and remove generic AI-generated patterns.
```

---

### Mode 3: Major Rework

Use when score is 4–5.9.

Focus on:

- Reworking layout
- Rebuilding hero
- Reordering sections
- Replacing generic structures
- Stronger brand direction
- Better conversion flow

Prompt phrase:

```txt
Use the current concept only as a rough direction. Rework the layout, hierarchy, content rhythm, and visual structure while preserving the core Design DNA.
```

---

### Mode 4: Regenerate From Strategy

Use when score is below 4.

Focus on:

- Starting fresh
- Keeping only brief/UX/DNA
- Discarding current UI
- Generating a better concept

Prompt phrase:

```txt
Discard the current UI concept. Generate a new version using the original brief, UX strategy, and Design DNA. Do not preserve the current layout.
```

---

## Humanization Patterns

Use these patterns to improve AI-generated UI.

---

### Pattern 1: Replace Generic Feature Cards

Instead of:

```txt
Three equal cards with icons and short text.
```

Use:

```txt
A varied feature storytelling section with one large primary feature, two compact supporting points, and one proof metric.
```

---

### Pattern 2: Improve Hero

Instead of:

```txt
Centered headline, generic subheading, two buttons, abstract graphic.
```

Use:

```txt
A hero with a specific promise, one strong CTA, one trust signal, and either product context, editorial imagery, or a meaningful visual demonstration.
```

---

### Pattern 3: Add Proof Earlier

Instead of:

```txt
Testimonials near the bottom only.
```

Use:

```txt
Add a small trust strip or metric row directly below the hero.
```

---

### Pattern 4: Make Sections Feel Designed

Instead of:

```txt
All sections using same card layout.
```

Use:

```txt
Alternate section structures: split layout, proof strip, comparison block, timeline, FAQ, final CTA.
```

---

### Pattern 5: Make Copy Specific

Instead of:

```txt
Powerful tools for your business.
```

Use:

```txt
Create client-ready proposals, track approval status, and follow up with warm leads from one workspace.
```

---

### Pattern 6: Reduce Decoration

Instead of:

```txt
More gradients, glowing cards, background blobs.
```

Use:

```txt
Cleaner hierarchy, stronger typography, restrained accent usage, and more intentional whitespace.
```

---

## Project-Type Refinement Guidance

### A. Landing Page

Common fixes:

- Strengthen hero headline
- Make primary CTA clearer
- Move proof higher
- Replace repeated features
- Add objection handling
- Improve final CTA
- Make form easier

### B. SaaS Dashboard

Common fixes:

- Reduce cognitive load
- Prioritize key metrics
- Improve navigation clarity
- Make actions more obvious
- Replace fake data with realistic modules
- Add empty/loading/error states

### C. Admin Panel

Common fixes:

- Improve table scanning
- Make filters/search stronger
- Clarify bulk actions
- Improve status labels
- Add confirmation states
- Reduce decoration

### D. Ecommerce

Common fixes:

- Improve product hierarchy
- Make pricing clearer
- Strengthen product cards
- Improve filters
- Add trust signals
- Simplify checkout path

### E. Mobile App

Common fixes:

- Improve thumb-friendly layout
- Make CTA sticky or easier to reach
- Reduce text density
- Improve bottom navigation
- Improve empty states
- Make feedback states clearer

---

## Quality Checklist

Before finalizing the refinement prompt, check:

- [ ] Does it preserve the strongest parts?
- [ ] Does it clearly state what to improve?
- [ ] Does it clearly state what to remove?
- [ ] Does it address AI-smell issues?
- [ ] Does it improve layout rhythm?
- [ ] Does it improve visual hierarchy?
- [ ] Does it improve content realism?
- [ ] Does it improve CTA clarity?
- [ ] Does it respect the Design DNA?
- [ ] Does it avoid random new styles?
- [ ] Is it ready to paste into Google Stitch?
- [ ] Does it include final quality instructions?

---

## Anti-Patterns To Avoid

Do not:

- Say only “make it more premium.”
- Add more decoration as a default fix.
- Introduce unrelated new color palettes.
- Introduce unrelated typography styles.
- Ignore the critique report.
- Ignore the Design DNA.
- Preserve weak sections without reason.
- Remove strong parts unnecessarily.
- Ask Stitch to “try again” without specific instructions.
- Fix everything visually while ignoring conversion.
- Use generic improvement language.
- Create a completely new prompt unless the concept score is very low.

---

## Example Trigger Phrases

Use this skill when the user says:

- “Humanize this UI.”
- “Make this less AI-generated.”
- “Create a refinement prompt.”
- “Improve this Stitch result.”
- “Turn this critique into a better prompt.”
- “Make it more premium.”
- “Make it more custom.”
- “Generate the next iteration prompt.”
- “Refine this concept.”
- “Fix the AI smell.”

---

## Example Output

```md
# Humanization & Refinement Plan

## 1. Refinement Objective

**Current UI Score:** 7.1/10  
**Primary Refinement Goal:** Make the landing page feel more custom, editorial, and premium while improving CTA clarity.  
**Main Problem To Solve:** The concept has a good luxury direction but still uses repeated feature cards and generic copy.  
**Desired Result:** A more human-designed, refined landing page with stronger proof, better section rhythm, and more realistic service content.

---

## 2. Preserve

Keep these parts of the current concept:

- Warm neutral color palette.
- Spacious hero direction.
- Image-led premium mood.
- Consultation-focused conversion goal.

---

## 3. Improve

Improve these areas:

- Hero CTA hierarchy.
- Section rhythm after the hero.
- Portfolio proof placement.
- Service copy realism.
- Final consultation CTA.

---

## 4. Remove / Reduce

Remove or reduce these AI-generated or weak elements:

- Repeated 3-card feature sections.
- Generic line icons.
- Overused phrases like “Transform your space.”
- Same-height section rhythm.
- Excessive accent color usage.

---

## 10. Google Stitch Refinement Prompt

Copy and paste this prompt into Google Stitch:

---

Refine the previous UI concept.

## Keep

- The warm neutral luxury palette.
- The spacious hero composition.
- The image-led premium direction.
- The primary goal of booking consultations.

## Improve

- Make the hero CTA more visually clear without making it loud.
- Move visual proof or featured project content higher on the page.
- Make the layout feel more editorial and less template-like.
- Improve the realism of service copy and section headings.
- Create stronger rhythm between sections.

## Remove / Avoid

- Repeated 3-card feature sections.
- Generic icons that do not add meaning.
- Purple-blue gradients, glassmorphism, blobs, or decorative AI-style effects.
- Overused luxury copy and vague marketing lines.
- Same-height repetitive sections.

## Layout Changes

- Replace one generic feature grid with a split editorial section: large image on one side, focused service explanation on the other.
- Add a compact trust/proof strip below the hero.
- Use a process timeline instead of another card grid.
- Make the final CTA feel like a calm consultation invitation, not a banner ad.

## Visual Changes

- Reduce accent color usage and reserve it for primary CTAs and small highlights.
- Use thin borders and whitespace instead of heavy shadows.
- Keep typography elegant and readable.
- Use consistent radius across cards, buttons, and form fields.

## Content Changes

- Replace generic phrases with specific interior design service language.
- Use realistic headings like “From first consultation to final handover.”
- Add believable proof points such as “Turnkey execution,” “Material selection support,” and “Project timeline clarity.”
- Make CTA copy direct: “Book a Design Consultation.”

## Interaction & Motion Changes

- Use subtle image hover and soft section reveal.
- Avoid bouncy or decorative animation.
- Keep transitions refined and slow enough to feel premium but not delayed.

## Maintain Design System

Keep the same:
- Core color palette
- Typography direction
- Brand tone
- Button style
- Card radius
- Spacing discipline
- Navigation structure, unless listed as an issue

Do not introduce unrelated new styles.

## Anti-AI Rules

Avoid:
- Repeated 3-card layouts
- Generic placeholder content
- Decorative blobs
- Random gradients
- Unnecessary glassmorphism
- Fake dashboards or fake data
- Inconsistent shadows
- Inconsistent border radius
- Overuse of icons
- Same-height repetitive sections

## Final Quality Instruction

Make the UI feel more intentional, premium, brand-specific, conversion-focused, and human-crafted. The refined version should feel like it was improved by a senior UI/UX designer, not regenerated randomly.
```


---

## Project Memory Behavior

**Skill Number:** 06
**Skill Role:** Humanization & Refinement — reads critique and Design DNA, produces refinement prompt.

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
- `.agency/UI_CRITIQUE.md`
- `.agency/DESIGN_DNA.md`

### Skill Output Files

After completing this skill, write output to:

- `.agency/REFINEMENT_PROMPT.md` — the Humanization & Refinement Plan and Stitch prompt
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

1. Save the Humanization & Refinement Plan to `.agency/REFINEMENT_PROMPT.md`.
2. Update `.agency/CURRENT_CONTEXT.md` with current phase, completed items, and next step.
3. Update `.agency/PROJECT_STATE.json`.
4. Update `.agency/CONTEXT_INDEX.json`:
   - Set `current_phase` to `humanization`
   - Set `current_skill` to `responsive-accessibility-review`
   - Set `required_context_files` to `[".agency/CURRENT_CONTEXT.md", ".agency/DESIGN_DNA.md", ".agency/PROJECT_STATE.json"]`
5. Append a short entry to `.agency/CHANGELOG.md`.
6. Update `.agency/TODO.md` with next steps.
7. Add major refinement decisions to `.agency/DECISIONS.md`.
8. Do not delete previous decisions or changelog entries.
