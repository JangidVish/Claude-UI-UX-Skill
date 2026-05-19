---
skill_id: uiux-persona-jtbd
skill_number: 01.5
requires_visual_input: false
requires_browser: false
project_complexity: standard, full
human_checkpoint_after: false
output_file: .agency/PERSONAS.md
reads_from:
  - .agency/CLIENT_BRIEF.md
  - .agency/COMPETITIVE_ANALYSIS.md
---

# Persona & JTBD Skill

## Purpose

This skill converts the Client Brief into proto-personas and Jobs-To-Be-Done statements that inform every design decision downstream.

Not fictional marketing personas with stock photos and made-up names. Research-grounded behavior models: who the user is, what they are trying to accomplish, what stops them, and what would make them trust and convert.

The output feeds directly into:

- UX Strategy — informs user journey and page hierarchy
- Design DNA — informs tone, visual language, and emotional targets
- Content Strategy — informs voice, copy, and pain-point framing

---

## When To Use

- After Client Discovery
- Before UX Strategy
- On standard and full projects
- When the client's audience is not clearly defined
- When multiple user types exist (different needs, different journeys)
- When competitive analysis reveals an audience the client has not considered

Skip for lite projects. Mark `personas.status` as `skipped` in `PROJECT_STATE.json`.

---

## Core Behavior

When triggered:

1. Read `CLIENT_BRIEF.md` — extract audience details, pain points, motivations, technical comfort level, and expected emotional response.
2. Read `COMPETITIVE_ANALYSIS.md` if it exists — look for gaps in how competitors serve the audience.
3. Identify how many distinct user types exist (1–3 maximum for most projects).
4. Build a proto-persona for each user type.
5. Write a JTBD statement for each persona.
6. Write a friction audit: what stops each persona from converting.
7. Write a design implication for each persona finding.

---

## Proto-Persona vs. Full Persona

This skill builds **proto-personas** — not full research-based personas. The difference:

| Type | Based On | Time |
|---|---|---|
| Full Persona | Interviews, surveys, analytics | Days to weeks |
| Proto-Persona | Client brief, competitor analysis, domain knowledge | Minutes |

Proto-personas are clearly marked as assumptions. They are good enough to make better design decisions. They should be validated with real users when budget allows.

---

## How Many Personas To Build

| Project Type | Personas |
|---|---|
| Landing page / single CTA | 1 primary |
| Service website | 1–2 (buyer + researcher) |
| SaaS product | 1–3 (primary user, admin, evaluator) |
| Ecommerce | 1–2 (impulse buyer + deliberate buyer) |
| Marketplace | 2 (buyer + seller) |
| Booking platform | 2 (user + service provider) |

Never build more than 3 personas. More personas = diffused design = weak product.

---

## Proto-Persona Format

```md
## Persona [N]: [Persona Name]

> [One sentence that captures who this person is and what they want]

### Profile

| Attribute | Value |
|---|---|
| Role / Title | [e.g., "Homeowner planning a renovation"] |
| Age Range | [e.g., "32–48"] |
| Location | [e.g., "Urban / Tier 1 city"] |
| Technical Comfort | [Low / Medium / High] |
| Device Primary | [Desktop / Mobile / Both] |
| Income / Budget | [e.g., "Mid-to-high, value-conscious"] |

### What They Are Trying To Do

[2–3 sentences. The task or goal they arrive with. Not what the business wants them to do — what THEY want to do.]

### What They Know Before Arriving

[What research have they already done? What do they believe about the market? What assumptions do they arrive with?]

### What They Fear

- [Fear 1 — e.g., "Spending money on something that doesn't look as good as expected"]
- [Fear 2 — e.g., "Getting locked into a vendor who disappears mid-project"]
- [Fear 3]

### What Would Make Them Trust

- [Trust signal 1 — e.g., "Seeing work similar to their own project in the portfolio"]
- [Trust signal 2 — e.g., "Clear pricing or at least a pricing range"]
- [Trust signal 3]

### What Would Make Them Leave

- [Exit trigger 1 — e.g., "Can't find pricing or a clear next step within 30 seconds"]
- [Exit trigger 2 — e.g., "Generic copy that could belong to any competitor"]
- [Exit trigger 3]

### Emotional State On Arrival

[What is this person feeling when they land on the site? Excited? Skeptical? Tired from research? Urgency?]

### Success Looks Like

[What does this persona do when the design works? Books a call? Signs up? Adds to cart? What does a converted persona look like?]

### Quote (Representative Voice)

> "[Write a realistic sentence this person would say about their situation or need]"
```

---

## JTBD Format

Jobs-To-Be-Done captures the functional, emotional, and social dimensions of what a user hires a product to do.

Use this format for each persona:

```md
## JTBD: [Persona Name]

### Functional Job

When I [situation], I want to [motivation], so I can [outcome].

### Emotional Job

When I [situation], I want to feel [emotion], so that [why it matters].

### Social Job

When I [situation], I want others to [perceive me as], so that [social outcome].

---

### Job Map

| Stage | What The User Wants |
|---|---|
| Define | [What they need to figure out first] |
| Locate | [Where they go to find options] |
| Prepare | [What they do before committing] |
| Confirm | [What makes them decide] |
| Execute | [The conversion action] |
| Monitor | [What they track after converting] |
| Modify | [What they might need to change later] |
```

---

## Friction Audit

For each persona, identify the conversion blockers specific to this project.

```md
## Friction Audit: [Persona Name]

| Friction Point | Where It Happens | How To Remove It |
|---|---|---|
| [e.g., No price signal] | [Hero / Pricing section] | [Show "Starting from X" or "Packages from X"] |
| [e.g., Portfolio lacks similar projects] | [Portfolio section] | [Filter or label projects by type/industry] |
| [e.g., CTA is too aggressive too early] | [Hero] | [Replace "Buy Now" with "See How It Works"] |
```

---

## Design Implications

After completing all personas, write a consolidated design implications section.

```md
## Design Implications

These findings from the persona work must be reflected in the design:

1. [Implication] — [Which persona / which finding]
2. [Implication] — [Which persona / which finding]
3. [Implication] — [Which persona / which finding]
...

### Priority Hierarchy

If these personas have competing needs, prioritize in this order:

1. [Primary persona name] — primary conversion target
2. [Secondary persona name] — secondary target
3. [Tertiary persona name if applicable]

When design decisions conflict, favor the primary persona.
```

---

## Output Format

```md
# Personas & Jobs-To-Be-Done

_Generated by UI/UX Agency Skill System — Persona & JTBD Skill (01.5)_
_Note: These are proto-personas based on the client brief and domain knowledge. Validate with real user research when possible._

---

## Summary

**Number of Personas:** [N]
**Primary Persona:** [Name]
**Secondary Persona:** [Name or N/A]
**Key Design Anchor:** [The one user insight that must drive every major design decision]

---

[Proto-Persona blocks]

---

[JTBD blocks]

---

[Friction Audit blocks]

---

[Design Implications block]
```

---

## Validation Before Output

- [ ] Every persona has a realistic quote that sounds like a real person
- [ ] Every JTBD has all three dimensions (functional, emotional, social)
- [ ] Every friction point has a specific removal strategy
- [ ] Design implications are actionable, not abstract
- [ ] Personas are clearly marked as proto-personas (not research-validated)
- [ ] Persona names are descriptive roles, not stereotypes (e.g., "The Deliberate Researcher" not "Soccer Mom")
- [ ] No more than 3 personas built
- [ ] Priority hierarchy is explicit when personas have competing needs

---

## Naming Personas

Use role-based descriptive names that capture behavior, not demographics.

Good names:
- "The Deliberate Researcher" — evaluates for weeks before deciding
- "The Impatient Executor" — knows what they want, needs to act fast
- "The Skeptical Buyer" — high-value purchase, high fear of being burned
- "The Referral Arrival" — already trust-primed by a recommendation

Avoid:
- "Sarah, 34, marketing manager" — demographic-first, not behavior-first
- "Millennial" — too broad
- "Power User" — too vague

---

## Anti-Patterns To Avoid

- Building personas with no connection to the actual project goals
- Writing personas that all want the same thing (if so, you have one persona, not three)
- Making every persona "tech-savvy urban professional" — challenge assumptions from the brief
- Skipping the friction audit — it is the most actionable section
- Writing JTBD statements that describe what the company offers, not what the user wants
- Personas without a clear priority hierarchy

---

## Project Memory Behavior

**Skill Number:** 01.5
**Reads from:** `.agency/CLIENT_BRIEF.md`, `.agency/COMPETITIVE_ANALYSIS.md`
**Writes to:** `.agency/PERSONAS.md`

Before running:

1. Check `.agency/` exists.
2. Read `.agency/CURRENT_CONTEXT.md`.
3. Read `.agency/CONTEXT_INDEX.json`.
4. Read `CLIENT_BRIEF.md`.
5. Read `COMPETITIVE_ANALYSIS.md` if it exists (not required).
6. Do not read files not listed above.

---

## Session Resume Behavior

1. Do not ask user to repeat context.
2. Read `.agency/CURRENT_CONTEXT.md` and `CONTEXT_INDEX.json`.
3. Read `CLIENT_BRIEF.md`.
4. If `PERSONAS.md` already has partial content, continue from the last incomplete persona.
5. Do not rebuild personas already written.

---

## Post-Task Update Behavior

After completing this skill:

1. Save all personas, JTBD, friction audit, and design implications to `.agency/PERSONAS.md`.
2. Update `.agency/CURRENT_CONTEXT.md`:
   - Set current phase to `personas`
   - Mark personas as completed
   - Set next step to UX Strategy
3. Update `.agency/PROJECT_STATE.json`:
   - Set `personas.status` to `complete`
   - Set `personas.completed_at` to today's date
4. Update `.agency/CONTEXT_INDEX.json`:
   - Set `current_skill` to `ux-strategy`
   - Add `.agency/PERSONAS.md` to `required_context_files` for UX Strategy, Design DNA, and Content Strategy
5. Append entry to `.agency/CHANGELOG.md`.
6. Update `.agency/TODO.md`.
7. Add key audience insight decisions to `.agency/DECISIONS.md` — especially primary persona selection and priority hierarchy.
8. Do not delete previous content.

---

## Example Trigger Phrases

- "Build personas for this project."
- "Create the JTBD."
- "Who are the users for this project?"
- "Define the target audience personas."
- "Run persona research."
- "What are the Jobs-To-Be-Done for this brief?"
- "Create user personas before UX strategy."
