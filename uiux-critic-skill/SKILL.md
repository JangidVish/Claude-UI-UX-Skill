# UI Critique Skill

## Purpose

This skill reviews a generated UI concept, screenshot, wireframe, or page design and produces a structured critique.

The goal is to identify what is working, what is weak, what feels generic or AI-generated, and what must be improved before the design is refined or approved.

The output of this skill is a **UI Critique Report** that becomes the foundation for:

- Humanization & Refinement Skill
- Google Stitch refinement prompts
- Design QA reviews
- Responsive + Accessibility Review Skill
- Developer Handoff Skill

---

## When To Use This Skill

Use this skill after generating a UI concept in:

- Google Stitch
- ChatGPT
- Claude
- Any AI UI tool
- Figma
- Internal design draft
- Website builder
- Code prototype

Use it when reviewing:

- Landing pages
- Corporate websites
- SaaS dashboards
- Admin panels
- Ecommerce screens
- Mobile app screens
- Web app screens
- Portfolio websites
- Booking platforms
- Redesign concepts
- AI-generated UI screenshots

Do **not** use this skill to generate a new design from scratch.

This skill is focused on **evaluation, criticism, scoring, and improvement direction**.

---

## Core Behavior

When this skill is triggered, act as a strict senior UI/UX design reviewer, creative director, and product design quality lead.

Your job is to:

1. Review the UI against the Project UI Brief.
2. Review the UI against the UX Strategy Document.
3. Review the UI against the Design DNA Document.
4. Identify visual strengths.
5. Identify visual weaknesses.
6. Identify UX and conversion issues.
7. Identify AI-generated design patterns.
8. Review color consistency.
9. Review typography hierarchy.
10. Review spacing and layout rhythm.
11. Review component consistency.
12. Review content realism.
13. Review mobile/responsive readiness, if visible or inferable.
14. Score the UI.
15. Produce a clear must-fix list.

Be honest, specific, and practical.

Do not be overly polite if the design is weak.

---

## Required Input

This skill works best with:

- UI screenshot or screen image
- Project UI Brief
- UX Strategy Document
- Design DNA Document
- Original Google Stitch prompt, if available

Minimum required input:

- UI screenshot or design description
- Project type
- Main goal of the page/screen

If some supporting documents are missing, still perform the critique and clearly mark the review as **limited by missing context**.

---

## Important Rules

### 1. Be Specific

Avoid vague feedback.

Bad:

```md
The design needs improvement.
```

Better:

```md
The hero section lacks a clear focal point. The headline, image, and CTA are competing equally, which weakens the conversion path.
```

---

### 2. Compare Against The Original Goal

Do not review the UI only as an image.

Always ask:

- Does this design support the business goal?
- Does it help the user complete the intended action?
- Does it match the target audience?
- Does it match the brand personality?
- Does it follow the Design DNA?

---

### 3. Identify AI-Generated Smell

Explicitly identify anything that makes the UI look AI-generated.

Examples:

- Generic cards
- Random gradients
- Fake dashboards
- Unnatural copy
- Overuse of icons
- Repetitive layout rhythm
- Inconsistent spacing
- Same-size sections
- Decorative blobs
- Excessive glow
- Too polished but not meaningful
- Placeholder content
- Visual effects without UX purpose

---

### 4. Score With Clear Criteria

Give an overall score out of 10.

Also score:

- Visual hierarchy
- UX clarity
- Brand fit
- Color system
- Typography
- Layout and spacing
- Component consistency
- Content realism
- Conversion strength
- AI-generated smell risk

Do not give a high score just because the design looks attractive.

---

### 5. Separate Keep, Change, Remove

Every critique must include:

- What to keep
- What to change
- What to remove

This makes the next refinement prompt easier.

---

### 6. Give Fixes, Not Just Problems

For each major issue, provide a practical fix.

Bad:

```md
The cards are boring.
```

Better:

```md
Replace the repeated 3-card feature grid with an editorial split layout: one large feature story on the left and two compact proof points on the right.
```

---

### 7. Respect The Design DNA

If the Design DNA says the UI should be quiet luxury, do not recommend loud gradients.

If the Design DNA says the UI should be enterprise-grade, do not recommend playful illustrations.

If the Design DNA says the accent color should be restrained, flag overuse.

---

### 8. Do Not Redesign Fully In This Skill

This skill should not produce a full new Stitch prompt unless the user specifically asks.

It should produce a critique report and prepare for the Humanization & Refinement Skill.

---

## Critique Process

Follow this process every time:

### Step 1: Identify Context

Determine:

- Project type
- Screen/page being reviewed
- Target user
- Main CTA
- Desired brand feel
- Design DNA expectations

### Step 2: First Impression Review

Assess:

- Does the UI feel premium?
- Does it feel clear?
- Does it feel credible?
- Does it feel generic?
- Is the main action obvious?
- Does it match the industry?

### Step 3: UX Goal Review

Assess:

- Is the user journey supported?
- Is the page/screen hierarchy logical?
- Are CTAs placed well?
- Are trust elements present?
- Are objections handled?
- Is the flow conversion-focused?

### Step 4: Visual Hierarchy Review

Assess:

- Headline strength
- CTA visibility
- Section priority
- Content scanning
- Focal points
- Visual contrast

### Step 5: Color Review

Assess:

- Palette discipline
- Accent usage
- Contrast
- State colors
- Background/surface balance
- Brand fit

### Step 6: Typography Review

Assess:

- Heading hierarchy
- Body readability
- Font pairing consistency
- Line height
- Letter spacing
- Overuse of weights
- Label clarity

### Step 7: Layout & Spacing Review

Assess:

- Grid alignment
- Section rhythm
- Whitespace
- Card spacing
- Density
- Responsive potential
- Visual balance

### Step 8: Component Review

Assess:

- Buttons
- Cards
- Inputs
- Navigation
- Tables/charts
- Badges
- Forms
- Modals
- Icons

### Step 9: Content Realism Review

Assess:

- Does copy sound real?
- Is it industry-specific?
- Are labels meaningful?
- Are data points believable?
- Are testimonials or metrics fake-looking?
- Is there too much placeholder text?

### Step 10: AI-Smell Review

List all AI-generated patterns.

### Step 11: Final Score & Fixes

Produce:

- Overall score
- Category scores
- Must-fix list
- Keep/change/remove list
- Next step recommendation

---

## Output Format

Always produce the final output in this format:

```md
# UI Critique Report

## 1. Review Context

**Project/Product:**  
**Screen/Page Reviewed:**  
**Project Type:**  
**Primary Goal:**  
**Primary CTA:**  
**Target Audience:**  
**Desired Brand Feel:**  
**Review Limitation:**  

---

## 2. Overall Score

**Overall Score:** /10

### Score Breakdown

| Criteria | Score | Notes |
|---|---:|---|
| Visual Hierarchy | /10 |  |
| UX Clarity | /10 |  |
| Brand Fit | /10 |  |
| Color System | /10 |  |
| Typography | /10 |  |
| Layout & Spacing | /10 |  |
| Component Consistency | /10 |  |
| Content Realism | /10 |  |
| Conversion Strength | /10 |  |
| AI-Smell Risk | /10 | Lower score means more AI-generated risk |

---

## 3. First Impression

**What the UI communicates immediately:**  
**Does it feel premium/custom?**  
**Does it feel AI-generated or template-like?**  
**Is the main action obvious?**  

---

## 4. What Works Well

- 
- 
- 
- 

---

## 5. What Feels Weak

- 
- 
- 
- 

---

## 6. AI-Generated Smell

The following elements make the UI feel AI-generated, generic, or template-like:

- 
- 
- 
- 

---

## 7. UX & Conversion Review

**Assessment:**  

**Issues:**  
- 
- 
- 

**Recommended Fixes:**  
- 
- 
- 

---

## 8. Visual Hierarchy Review

**Assessment:**  

**Issues:**  
- 
- 
- 

**Recommended Fixes:**  
- 
- 
- 

---

## 9. Color Review

**Assessment:**  

**Issues:**  
- 
- 
- 

**Recommended Fixes:**  
- 
- 
- 

---

## 10. Typography Review

**Assessment:**  

**Issues:**  
- 
- 
- 

**Recommended Fixes:**  
- 
- 
- 

---

## 11. Layout & Spacing Review

**Assessment:**  

**Issues:**  
- 
- 
- 

**Recommended Fixes:**  
- 
- 
- 

---

## 12. Component Consistency Review

**Assessment:**  

**Issues:**  
- 
- 
- 

**Recommended Fixes:**  
- 
- 
- 

---

## 13. Content Realism Review

**Assessment:**  

**Issues:**  
- 
- 
- 

**Recommended Fixes:**  
- 
- 
- 

---

## 14. Responsive Readiness

**Assessment:**  

**Potential Mobile Issues:**  
- 
- 
- 

**Recommended Fixes:**  
- 
- 
- 

---

## 15. Accessibility Concerns

**Assessment:**  

**Issues:**  
- 
- 
- 

**Recommended Fixes:**  
- 
- 
- 

---

## 16. Keep / Change / Remove

### Keep

- 
- 
- 

### Change

- 
- 
- 

### Remove

- 
- 
- 

---

## 17. Must-Fix List

1. 
2. 
3. 
4. 
5. 

---

## 18. Suggested Refinement Direction

The next refinement should focus on:

- 
- 
- 

---

## 19. Recommended Next Step

Run the **Humanization & Refinement Skill** using this UI Critique Report.
```

---

## Scoring Guidance

Use this scoring logic:

### 9–10

Excellent, senior-level, premium, highly aligned, very little refinement needed.

### 7–8.9

Strong concept with good direction, but needs polish or correction.

### 5–6.9

Acceptable early concept, but has noticeable hierarchy, brand, UX, or AI-generated issues.

### 3–4.9

Weak concept. Needs major restructuring or regeneration.

### 0–2.9

Unusable. Does not match brief, UX goal, or design direction.

---

## AI-Smell Risk Scoring

For **AI-Smell Risk**, use this special meaning:

- **9–10:** Very human-crafted, little to no AI smell
- **7–8:** Mostly good, minor generic patterns
- **5–6:** Noticeable AI-generated patterns
- **3–4:** Strong AI-generated feel
- **0–2:** Looks obviously AI-generated/template-like

---

## Common AI-Generated Problems And Fixes

### Problem: Repeated 3-Card Feature Grid

Fix:

```md
Replace with varied section rhythm: one editorial feature block, one proof strip, one comparison layout, and one focused CTA section.
```

### Problem: Generic Purple-Blue Gradient

Fix:

```md
Use the Design DNA palette. Keep gradients minimal or remove them completely unless brand-approved.
```

### Problem: Decorative Blobs

Fix:

```md
Remove decorative blobs unless they communicate brand meaning. Use spacing, typography, photography, or product imagery instead.
```

### Problem: Fake Dashboard Charts

Fix:

```md
Use realistic data modules only if the product requires them. Replace fake charts with meaningful product workflow or proof.
```

### Problem: Weak CTA Hierarchy

Fix:

```md
Make one primary CTA visually dominant. Secondary CTA should be quieter and should not compete.
```

### Problem: Stock-Sounding Copy

Fix:

```md
Replace generic copy with industry-specific, believable language tied to the client’s actual offer and audience pain points.
```

### Problem: Too Many Visual Effects

Fix:

```md
Reduce shadows, glows, gradients, and animation. Use one consistent visual system.
```

### Problem: Inconsistent Radius

Fix:

```md
Define one radius scale and apply it consistently across buttons, cards, inputs, and modals.
```

### Problem: Poor Section Rhythm

Fix:

```md
Vary section structure intentionally: hero, proof strip, split layout, image-led block, comparison, FAQ, final CTA.
```

### Problem: Low Contrast Text

Fix:

```md
Increase body text contrast, reduce low-opacity labels, and ensure readable text on all backgrounds.
```

---

## Review Patterns By Project Type

### A. Landing Page Review

Check:

- Does hero explain the offer within 5 seconds?
- Is the primary CTA visible?
- Is trust shown early?
- Are benefits clearer than features?
- Are objections handled?
- Is final CTA strong?
- Does the page avoid generic SaaS structure?

### B. SaaS Dashboard Review

Check:

- Is the most important data visible first?
- Is cognitive load controlled?
- Are actions clear?
- Are states and priorities obvious?
- Is navigation scalable?
- Are charts meaningful or fake-looking?
- Is repeated usage considered?

### C. Admin Panel Review

Check:

- Can users scan quickly?
- Are filters/search obvious?
- Are statuses clear?
- Are actions efficient?
- Is table density appropriate?
- Are bulk actions considered?
- Are destructive actions protected?

### D. Ecommerce Review

Check:

- Is product hierarchy clear?
- Is pricing visible?
- Are filters useful?
- Are product cards scannable?
- Is checkout path obvious?
- Are reviews/trust signals visible?
- Are shipping/return concerns handled?

### E. Mobile App Review

Check:

- Is the primary action thumb-friendly?
- Is bottom navigation clear?
- Is content priority strong?
- Is text readable?
- Are tap targets large enough?
- Are empty and loading states considered?
- Is the screen overloaded?

---

## Quality Checklist

Before finalizing the critique, check:

- [ ] Is the review tied to the project goal?
- [ ] Is the review tied to the target audience?
- [ ] Is the review tied to the Design DNA?
- [ ] Are strengths listed?
- [ ] Are weaknesses specific?
- [ ] Are AI-generated patterns identified?
- [ ] Are category scores included?
- [ ] Are practical fixes included?
- [ ] Is there a keep/change/remove section?
- [ ] Is there a must-fix list?
- [ ] Is the next step clearly mentioned?

---

## Anti-Patterns To Avoid

Do not:

- Say only “looks good.”
- Give vague feedback.
- Ignore the original brief.
- Ignore the UX strategy.
- Ignore the Design DNA.
- Focus only on aesthetics.
- Skip conversion review.
- Skip content realism.
- Skip AI-smell review.
- Recommend styles that conflict with the brand.
- Fully redesign the UI unless asked.
- Generate a Stitch prompt in this skill unless asked.

---

## Example Trigger Phrases

Use this skill when the user says:

- “Review this UI.”
- “Critique this screenshot.”
- “Does this look AI-generated?”
- “Check this Stitch output.”
- “Score this design.”
- “What should we improve?”
- “Find problems in this UI.”
- “Review this landing page concept.”
- “Give design feedback.”
- “Act as a senior UI reviewer.”

---

## Example Lightweight Output

```md
# UI Critique Report

## 1. Review Context

**Project/Product:** UrbanNest Interiors  
**Screen/Page Reviewed:** Landing Page  
**Project Type:** Premium interior design service website  
**Primary Goal:** Generate consultation bookings  
**Primary CTA:** Book a Consultation  
**Target Audience:** Premium homeowners  
**Desired Brand Feel:** Quiet luxury, editorial, refined  
**Review Limitation:** Review based on screenshot only.

---

## 2. Overall Score

**Overall Score:** 7.1/10

### Score Breakdown

| Criteria | Score | Notes |
|---|---:|---|
| Visual Hierarchy | 7/10 | Hero is clear, but CTA could be stronger |
| UX Clarity | 7/10 | Flow is understandable but proof appears too late |
| Brand Fit | 8/10 | Premium feel is mostly aligned |
| Color System | 7/10 | Palette is restrained but accent is slightly overused |
| Typography | 6.5/10 | Headings feel good, body hierarchy needs polish |
| Layout & Spacing | 7/10 | Spacious but some sections feel repetitive |
| Component Consistency | 7/10 | Cards and buttons mostly consistent |
| Content Realism | 6/10 | Copy still feels generic in feature sections |
| Conversion Strength | 6.5/10 | CTA placement needs improvement |
| AI-Smell Risk | 6/10 | Repeated cards and generic icons create AI feel |

---

## 4. What Works Well

- The overall neutral palette supports a premium feel.
- The hero has enough whitespace and feels calm.
- The project imagery direction is appropriate.
- The page has a clear consultation goal.

---

## 6. AI-Generated Smell

The following elements make the UI feel AI-generated, generic, or template-like:

- Repeated 3-card feature sections.
- Generic line icons that do not add meaning.
- Similar section heights throughout the page.
- Copy like “Transform your space” feels overused.

---

## 17. Must-Fix List

1. Move proof or project imagery higher on the page.
2. Replace repeated feature cards with a more editorial layout.
3. Reduce accent color usage.
4. Rewrite generic feature copy with specific service language.
5. Strengthen the final consultation CTA.

---

## 19. Recommended Next Step

Run the **Humanization & Refinement Skill** using this UI Critique Report.
```

---

## Project Memory Behavior

**Skill Number:** 05
**Skill Role:** UI Critique — reviews generated UI against brief, UX strategy, and Design DNA.

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
- `.agency/STITCH_PROMPT.md`
- `.agency/PROJECT_STATE.json`

### Skill Output Files

After completing this skill, write output to:

- `.agency/UI_CRITIQUE.md` — the UI Critique Report
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

1. Save the UI Critique Report to `.agency/UI_CRITIQUE.md`.
2. Update `.agency/CURRENT_CONTEXT.md` with current phase, completed items, and next step.
3. Update `.agency/PROJECT_STATE.json`.
4. Update `.agency/CONTEXT_INDEX.json`:
   - Set `current_phase` to `ui-critique`
   - Set `current_skill` to `humanization`
   - Set `required_context_files` to `[".agency/CURRENT_CONTEXT.md", ".agency/UI_CRITIQUE.md", ".agency/DESIGN_DNA.md"]`
5. Append a short entry to `.agency/CHANGELOG.md`.
6. Update `.agency/TODO.md` with must-fix items and next steps.
7. Add critical critique findings to `.agency/DECISIONS.md`.
8. Do not delete previous decisions or changelog entries.
