---
skill_id: uiux-client-presentation
skill_number: 10
requires_visual_input: false
requires_browser: false
project_complexity: standard, full
human_checkpoint_after: false
output_file: .agency/CLIENT_PRESENTATION.md
reads_from:
  - .agency/CLIENT_BRIEF.md
  - .agency/UX_STRATEGY.md
  - .agency/DESIGN_DNA.md
  - .agency/DESIGN_DIRECTION_OPTIONS.md
  - .agency/UI_CRITIQUE.md
  - .agency/DECISIONS.md
---

# Client Presentation Skill

## Purpose

This skill assembles all completed project work into a structured client-facing presentation document.

It translates agency thinking into language the client understands: what we learned about their business, what we decided and why, what the design does for their users, and what happens next.

Use this skill before client review meetings, design approval calls, or handoff to a client's internal team.

---

## When To Use

- Before a design review or client presentation meeting
- When client needs to approve design direction before build
- When handing a project to another agency, freelancer, or client's team
- When a stakeholder not involved in discovery needs to get up to speed
- When creating a project portfolio case study

---

## Core Behavior

When triggered:

1. Read all available `.agency/` files listed in `reads_from`.
2. Identify what is completed vs. pending.
3. Translate technical design decisions into client-friendly language.
4. Structure content in presentation order: context → strategy → design → decisions → next steps.
5. Never use design jargon the client may not understand without a brief explanation.
6. Keep every section focused on client outcomes, not agency process.

---

## Presentation Structure

```md
# [Project Name] — Design Presentation

**Prepared for:** [Client Name]
**Prepared by:** [Agency Name]
**Date:** [Today's Date]
**Project Phase:** [Current Phase]

---

## 1. What We Understood

[Restate the client's business, audience, and goal in plain language. Show the client that you listened.]

### Your Business
[2–3 sentences about the business in the client's language]

### Your Audience
[Who are the users. What they need. What stops them from converting.]

### The Goal We Designed For
[State the single primary conversion goal and why it is the design anchor]

---

## 2. The Strategy

[Explain the UX decisions at a high level. No jargon. Client-friendly rationale.]

### How Users Move Through The Experience
[Describe the conversion flow in plain steps: arrives → sees → reads → acts]

### What We Prioritized Above The Fold
[Why hero section was built the way it was]

### Why The Navigation Works This Way
[If any non-obvious navigation decisions were made]

### How Trust Is Built
[Which design choices build credibility and reduce user objections]

---

## 3. The Design Direction

[Describe the chosen visual direction in accessible language — what it feels like, what it communicates, why it was chosen]

### Why This Direction
[Client-friendly rationale — why this look fits the brand and audience]

### What It Communicates To Users
[How users will perceive the brand on first impression]

### Key Visual Decisions

| Decision | What We Did | Why |
|---|---|---|
| Color Palette | [description] | [client-friendly reason] |
| Typography | [description] | [reason] |
| Layout Approach | [description] | [reason] |
| Photography Style | [description] | [reason] |

---

## 4. Pages & Sections Designed

[List what was designed, what each section does, and what the CTA is]

### [Page Name]

| Section | Purpose | CTA |
|---|---|---|
| Hero | [what it does] | [CTA text] |
| [Section] | [what it does] | [CTA text] |

Repeat per page.

---

## 5. Key Decisions Made

[Surface the most important decisions from DECISIONS.md, translated to client language]

| Decision | What We Decided | Why It Matters |
|---|---|---|
| [Decision] | [What was chosen] | [Impact on client outcomes] |

---

## 6. What Is Still Open

[Be transparent about open questions or pending approvals]

| Item | Status | What's Needed |
|---|---|---|
| [Item] | Pending client input | [What client must decide or provide] |
| [Item] | Pending content | [What copy/images are still needed] |

---

## 7. What Happens Next

[Clear next steps — what the agency will do, what the client must do, and by when]

### Agency's Next Steps
1. [Step]
2. [Step]
3. [Step]

### Client's Next Steps
1. [Step — what the client needs to provide, approve, or decide]
2. [Step]

### Timeline
| Phase | What Happens | Target Date |
|---|---|---|
| [Phase] | [Description] | [Date or TBD] |

---

## 8. How To Give Feedback

[Tell the client exactly how to give feedback so revisions are efficient]

**Use this format for feedback:**

Page: [which page]
Section: [which section]
Change: [what to change]
Reason: [why — optional but helpful]

**Avoid:**
- "Make it more modern" — too vague
- "I want blue" — without context

**Helpful:**
- "The hero headline feels too casual for our audience — can we make it more authoritative?"
- "On mobile the CTA button is hard to tap — can it be larger?"

---

## Appendix: Assumptions Made

[List all assumptions from the project — pulled from CLIENT_BRIEF.md]

- Assumption 1
- Assumption 2

---

## Appendix: Design Risks Flagged

[Pulled from CLIENT_BRIEF.md design risks section]

- Risk 1
- Risk 2
```

---

## Writing Rules

### 1. Never Use Unexplained Design Terms

If you must use a design term, define it immediately.

Wrong: "We used a hero section with a split layout and negative space to balance visual weight."
Right: "The top section uses a two-column layout — image on one side, text on the other — so users see the product and read the headline at the same time."

### 2. Frame Every Decision In Client Outcomes

Wrong: "We selected a sans-serif typeface for legibility and modern aesthetic."
Right: "We chose this font because it looks clean on all screens and reads easily on mobile, where most of your users are."

### 3. Acknowledge Open Items Honestly

Do not hide pending decisions or missing assets. Clients appreciate transparency.

### 4. Keep Sections Short

Clients will skim this. Use:
- Short paragraphs (3 sentences max per block)
- Tables for structured information
- Bullet points over long paragraphs

### 5. End Every Page Section With What The User Does Next

After describing what a page does, always state what the next action is. Connects design to conversion.

---

## Slide Outline (Optional)

If the client wants a slide deck, map the sections to slides:

| Slide | Content |
|---|---|
| 1 | Title + project name + agency logo |
| 2 | What we understood: business + audience + goal |
| 3 | The strategy: user flow diagram (text-based) |
| 4 | Visual direction: mood + color + font |
| 5 | Key visual decisions table |
| 6 | Page walkthrough: Homepage |
| 7 | Page walkthrough: [other pages] |
| 8 | Key decisions made |
| 9 | Open items + what's needed from client |
| 10 | Next steps + timeline |

---

## Validation

Before writing the final output, check:

- [ ] Every design decision has a client-friendly rationale
- [ ] No unexplained design jargon
- [ ] Every page/screen is described
- [ ] Open items are listed honestly
- [ ] Next steps are specific (who does what)
- [ ] Feedback format is explained
- [ ] Assumptions from brief are listed
- [ ] Document reads from client's perspective, not agency's

---

## Project Memory Behavior

**Skill Number:** 10
**Reads from:** `.agency/CLIENT_BRIEF.md`, `.agency/UX_STRATEGY.md`, `.agency/DESIGN_DNA.md`, `.agency/DESIGN_DIRECTION_OPTIONS.md`, `.agency/UI_CRITIQUE.md`, `.agency/DECISIONS.md`
**Writes to:** `.agency/CLIENT_PRESENTATION.md`

Before running:

1. Check `.agency/` exists.
2. Read `.agency/CURRENT_CONTEXT.md`.
3. Read `.agency/CONTEXT_INDEX.json`.
4. Read required files listed above.
5. For files that do not exist, mark those sections as "Not yet completed" rather than skipping them silently.
6. Do not read files not listed above.

---

## Session Resume Behavior

1. Do not ask user to repeat context.
2. Read `.agency/CURRENT_CONTEXT.md` and `CONTEXT_INDEX.json`.
3. Read all `reads_from` files.
4. If `CLIENT_PRESENTATION.md` already has content, continue from the last incomplete section.
5. Do not restart the document if partial content exists.

---

## Post-Task Update Behavior

After completing this skill:

1. Save presentation to `.agency/CLIENT_PRESENTATION.md`.
2. Update `.agency/CURRENT_CONTEXT.md`:
   - Mark client-presentation as complete
   - Set next step to client review
3. Update `.agency/PROJECT_STATE.json`:
   - Set `client_presentation.status` to `complete`
4. Update `.agency/CONTEXT_INDEX.json`.
5. Append to `.agency/CHANGELOG.md`.
6. Update `.agency/TODO.md` — mark pending client input items.
7. Add any client approval decisions to `.agency/DECISIONS.md` when feedback comes in.
8. Do not delete previous content.

---

## Example Trigger Phrases

- "Create the client presentation."
- "Prepare the design review document."
- "Generate client deck."
- "Write the presentation for client approval."
- "Prepare handoff to client."
- "Create the project summary for the client."
- "We have a client review call — prepare the document."
