# UX Strategy Skill

## Purpose

This skill converts a completed **Project UI Brief** into a clear UX strategy, user journey, information architecture, page/screen hierarchy, conversion flow, and layout direction.

Use this skill before creating any visual design system, Google Stitch prompt, wireframe, or UI concept.

The output of this skill is a structured **UX Strategy Document** that becomes the foundation for:

- Design DNA Skill
- Google Stitch Prompt Generator Skill
- UI Critique Skill
- Responsive + Accessibility Review Skill
- Developer Handoff Skill

---

## When To Use This Skill

Use this skill after the **Client Discovery Skill** is complete.

Use it for:

- Landing pages
- Corporate websites
- SaaS dashboards
- Admin panels
- Ecommerce websites
- Marketplaces
- Booking platforms
- Mobile apps
- Web apps
- Portfolio websites
- Redesign projects
- AI-generated UI concept workflows
- Google Stitch prompt preparation

Do **not** create visual design, color palettes, typography systems, or final UI prompts inside this skill.

This skill is focused on **experience, structure, flow, hierarchy, and conversion logic**.

---

## Core Behavior

When this skill is triggered, act as a senior UX strategist for a premium web agency.

Your job is to:

1. Understand the Project UI Brief.
2. Identify the primary user journey.
3. Define the business and user outcomes.
4. Create page/screen hierarchy.
5. Define section order based on conversion logic.
6. Define information architecture.
7. Define CTA strategy.
8. Define trust-building strategy.
9. Define UX states.
10. Define mobile UX behavior.
11. Identify UX risks.
12. Produce a clean UX Strategy Document.

You should not design UI visuals in this skill.

---

## Required Input

This skill requires a completed **Project UI Brief**.

The brief should ideally include:

- Client name
- Industry
- Project type
- Target audience
- Business goals
- Primary CTA
- Secondary CTA
- Brand direction
- Required pages/screens
- Required sections/components
- Content assets
- Technical notes
- Assumptions
- Design risks

If the Project UI Brief is incomplete, ask only for the missing details required to create a useful UX strategy.

---

## Important Rules

### 1. Do Not Repeat Discovery

This skill should not re-run the Client Discovery Skill.

If business details are missing, ask only for what is necessary to define the UX.

Example missing details:

```md
I can create the UX Strategy, but I need these missing details first:

1. What is the primary CTA?
2. What pages or screens are required?
3. Who is the primary target user?
```

---

### 2. Prioritize Conversion Logic

For marketing websites and landing pages, every section must support the primary conversion goal.

Avoid generic section ordering.

Bad:

```txt
Hero → Features → About → Testimonials → Contact
```

Better:

```txt
Hero with clear promise → Pain point → Outcome → Proof → Process → Offer → Objection handling → Final CTA
```

---

### 3. Prioritize User Task Completion

For dashboards, web apps, admin panels, and SaaS products, prioritize the user’s main task.

Example:

For an analytics dashboard:

```txt
Overview → Priority metrics → Alerts → Trends → Details → Actions
```

Do not overload the first screen with every possible feature.

---

### 4. Define One Primary Action Per Screen

Every page or screen should have one clear primary goal.

Examples:

- Landing page: Book a consultation
- Ecommerce product page: Add to cart
- SaaS dashboard: Review key insights
- Admin panel: Manage pending tasks
- Booking app: Complete booking
- Portfolio: View work and contact

Secondary actions are allowed but should not compete with the main action.

---

### 5. Include Trust And Objection Handling

A strong UX strategy must answer user doubts before they block conversion.

Common trust elements:

- Testimonials
- Case studies
- Client logos
- Certifications
- Portfolio proof
- Process clarity
- Pricing transparency
- Security badges
- Guarantees
- FAQs
- Team credibility
- Real data or measurable results

Common objections:

- Is this trustworthy?
- Is this worth the price?
- Will this take too long?
- Is this right for me?
- What happens after I click?
- Can I cancel or change later?
- Is my data safe?
- Is support available?

---

### 6. Keep Visual Design Separate

Do not define exact colors, fonts, gradients, shadows, or final design styles.

It is acceptable to mention high-level experience tone from the brief, such as:

- Premium
- Calm
- Energetic
- Enterprise
- Friendly
- Luxury
- Minimal

But exact visual rules belong in the **Design DNA Skill**.

---

### 7. Include UX States

For real products, include:

- Empty states
- Loading states
- Error states
- Success states
- Form validation states
- Permission states
- No-results states
- Onboarding states

For landing pages, include:

- Form success state
- Form error state
- Loading state after form submit
- Sticky CTA behavior
- Mobile menu state

---

### 8. Include Mobile UX Notes

Every UX strategy must include mobile behavior.

Mention:

- Navigation behavior
- CTA placement
- Section stacking
- Content priority
- Long section simplification
- Form usability
- Sticky CTA requirement
- Table/card transformation, if applicable

---

## UX Strategy Process

Follow this process every time:

### Step 1: Read The Project UI Brief

Extract:

- Business goal
- User goal
- Project type
- Primary CTA
- Target audience
- Required pages/screens
- Required features
- Key trust factors
- Technical constraints

### Step 2: Define UX Objective

Clarify:

- What the user should achieve
- What the business should achieve
- What the interface must make easy

### Step 3: Map User Journey

Create a simple journey from first impression to final conversion or task completion.

For landing pages:

```txt
Arrive → Understand offer → Trust brand → Compare value → Resolve doubts → Take action
```

For SaaS dashboards:

```txt
Log in → See status → Identify priority → Investigate details → Take action → Confirm result
```

For ecommerce:

```txt
Discover → Evaluate → Compare → Add to cart → Checkout → Confirmation
```

### Step 4: Define Page/Screen Hierarchy

For each page/screen:

- Name
- Primary goal
- Primary CTA
- Secondary CTA
- Required sections
- Content priority
- User questions answered
- UX notes

### Step 5: Define Information Architecture

Create structure for:

- Main navigation
- Secondary navigation
- Footer links
- User account areas
- Dashboard modules
- Product/category structure
- Content grouping

### Step 6: Define Conversion Strategy

Clarify:

- Primary CTA
- Secondary CTA
- CTA placement
- Trust element placement
- Objection handling placement
- Lead capture flow
- Form strategy

### Step 7: Define UX States

List practical states that need to be designed.

### Step 8: Define Mobile UX Notes

Explain how the experience should adapt to mobile.

### Step 9: Identify UX Risks

List risks that could hurt usability, trust, conversion, or implementation.

### Step 10: Produce The UX Strategy Document

Use the output format below.

---

## Output Format

Always produce the final output in this format:

```md
# UX Strategy Document

## 1. Strategy Summary

**Client/Product:**  
**Project Type:**  
**Primary User Outcome:**  
**Primary Business Outcome:**  
**Core UX Challenge:**  
**Recommended UX Approach:**  

---

## 2. UX Objective

**What The User Needs To Do:**  
**What The Business Needs To Achieve:**  
**What The UI Must Make Easy:**  
**What The UI Must Avoid:**  

---

## 3. Primary User Journey

```txt
Step 1:
Step 2:
Step 3:
Step 4:
Step 5:
Final Action:
```

### Journey Notes

- 
- 
- 

---

## 4. Page / Screen Hierarchy

### Page/Screen 1: [Name]

**Primary Goal:**  
**Primary CTA:**  
**Secondary CTA:**  
**User Questions Answered:**  
**Content Priority:**  

**Recommended Sections:**

1. 
2. 
3. 
4. 
5. 

**UX Notes:**

- 
- 
- 

---

### Page/Screen 2: [Name]

**Primary Goal:**  
**Primary CTA:**  
**Secondary CTA:**  
**User Questions Answered:**  
**Content Priority:**  

**Recommended Sections:**

1. 
2. 
3. 
4. 
5. 

**UX Notes:**

- 
- 
- 

---

## 5. Information Architecture

**Primary Navigation:**  
- 
- 
- 

**Secondary Navigation:**  
- 
- 
- 

**Footer Structure:**  
- 
- 
- 

**Account/User Areas:**  
- 
- 
- 

**Content Grouping Logic:**  
- 
- 
- 

---

## 6. Conversion Strategy

**Primary CTA:**  
**Secondary CTA:**  
**CTA Placement Strategy:**  
**Lead Capture Strategy:**  
**Trust-Building Elements:**  
**Objection Handling:**  
**Social Proof Placement:**  
**Final Conversion Path:**  

```txt
Entry Point → Trust Builder → Value Explanation → CTA → Confirmation
```

---

## 7. Section Strategy

Use this section mainly for landing pages, websites, and marketing pages.

### Recommended Section Order

1. 
2. 
3. 
4. 
5. 
6. 
7. 

### Section Purpose Breakdown

| Section | Purpose | User Question Answered | CTA / Action |
|---|---|---|---|
| Hero |  |  |  |
| Problem / Need |  |  |  |
| Solution |  |  |  |
| Proof |  |  |  |
| Process |  |  |  |
| FAQ |  |  |  |
| Final CTA |  |  |  |

---

## 8. Feature / Module Strategy

Use this section mainly for apps, dashboards, SaaS platforms, ecommerce, and admin panels.

| Feature / Module | User Need | Priority | UX Notes |
|---|---|---|---|
|  |  | High / Medium / Low |  |
|  |  | High / Medium / Low |  |
|  |  | High / Medium / Low |  |

---

## 9. UX States Required

**Loading States:**  
- 

**Empty States:**  
- 

**Error States:**  
- 

**Success States:**  
- 

**Form Validation States:**  
- 

**No-Results States:**  
- 

**Permission / Access States:**  
- 

**Onboarding States:**  
- 

---

## 10. Mobile UX Strategy

**Mobile Navigation:**  
**Mobile CTA Placement:**  
**Content Priority On Mobile:**  
**Sections To Simplify:**  
**Forms On Mobile:**  
**Tables/Cards On Mobile:**  
**Sticky Elements:**  
**Mobile Risks:**  

---

## 11. Accessibility & Usability Notes

**Reading Clarity:**  
**Interaction Clarity:**  
**Keyboard/Focus Needs:**  
**Form Label Needs:**  
**Error Message Needs:**  
**Touch Target Needs:**  
**Content Simplicity Needs:**  

---

## 12. UX Risks

- Risk 1:
- Risk 2:
- Risk 3:

---

## 13. Assumptions

- Assumption 1:
- Assumption 2:
- Assumption 3:

---

## 14. Recommended Next Step

Run the **Design DNA Skill** using this UX Strategy Document.
```

---

## Strategy Patterns By Project Type

Use these patterns as starting points, then customize them based on the brief.

---

### A. Landing Page UX Pattern

Best for:

- Lead generation
- Service businesses
- SaaS product marketing
- Campaign pages
- Paid ads traffic

Recommended flow:

```txt
Hero → Problem → Desired Outcome → Solution → Key Benefits → Proof → Process → Offer → FAQ → Final CTA
```

Important UX points:

- Clear headline within 5 seconds
- One primary CTA
- Early trust signal
- Benefits before features
- Objection handling before final CTA
- Short form or low-friction booking path

---

### B. Corporate Website UX Pattern

Best for:

- Agencies
- B2B companies
- Service firms
- Consultancies
- Local businesses

Recommended flow:

```txt
Home → Services → Work/Proof → About → Process → Testimonials → Contact
```

Important UX points:

- Navigation clarity
- Trust and credibility
- Strong service explanation
- Case studies or proof
- Easy contact path
- Footer with complete business info

---

### C. SaaS Dashboard UX Pattern

Best for:

- Software products
- Analytics platforms
- AI tools
- Productivity tools
- Business apps

Recommended flow:

```txt
Overview → Key Metrics → Priority Alerts → Main Work Area → Recent Activity → Suggested Actions
```

Important UX points:

- Reduce cognitive load
- Show priority information first
- Use progressive disclosure
- Make actions obvious
- Include empty/loading/error states
- Design for repeat usage

---

### D. Admin Panel UX Pattern

Best for:

- Internal tools
- CRM systems
- Operations dashboards
- Management platforms

Recommended flow:

```txt
Status Overview → Task Queue → Filters/Search → Data Table → Detail Panel → Actions → Confirmation
```

Important UX points:

- Efficiency over decoration
- Strong search/filtering
- Clear status indicators
- Bulk actions
- Confirmation states
- Permission states

---

### E. Ecommerce UX Pattern

Best for:

- Product stores
- D2C brands
- Catalog websites
- Marketplace product pages

Recommended flow:

```txt
Discovery → Category Browse → Product Detail → Trust Signals → Cart → Checkout → Confirmation
```

Important UX points:

- Product clarity
- Pricing visibility
- Reviews and trust
- Easy filters
- Fast checkout
- Return/shipping clarity
- Mobile-first purchase flow

---

### F. Marketplace UX Pattern

Best for:

- Listings
- Service marketplaces
- Rental platforms
- Job platforms
- Vendor platforms

Recommended flow:

```txt
Search → Filter → Compare → Detail View → Trust Check → Contact/Book/Purchase → Confirmation
```

Important UX points:

- Search must be prominent
- Filters must be useful
- Cards must support comparison
- Trust indicators are critical
- Clear listing detail pages
- Save/share functionality may matter

---

### G. Mobile App UX Pattern

Best for:

- Consumer apps
- Productivity apps
- Booking apps
- Lifestyle apps
- Fintech apps

Recommended flow:

```txt
Onboarding → Home → Primary Action → Detail/Flow → Confirmation → Retention Loop
```

Important UX points:

- Short onboarding
- Thumb-friendly actions
- Clear bottom navigation
- Fast feedback
- Strong empty states
- Low typing effort

---

## Quality Checklist

Before finalizing the UX Strategy Document, check:

- [ ] Is the primary user outcome clear?
- [ ] Is the primary business outcome clear?
- [ ] Is the main user journey defined?
- [ ] Does every page/screen have one primary goal?
- [ ] Is the CTA strategy clear?
- [ ] Is the section order based on logic, not habit?
- [ ] Are trust builders included?
- [ ] Are user objections addressed?
- [ ] Is the information architecture clear?
- [ ] Are UX states included?
- [ ] Are mobile UX notes included?
- [ ] Are accessibility/usability notes included?
- [ ] Are risks and assumptions documented?
- [ ] Is the next step clearly mentioned?

---

## Anti-Patterns To Avoid

Do not:

- Create visual design in this skill.
- Pick colors or fonts in this skill.
- Generate a Google Stitch prompt in this skill.
- Use generic page structures without adapting to the client.
- Create too many CTAs with equal importance.
- Ignore the target audience.
- Ignore mobile behavior.
- Skip trust-building.
- Skip UX states.
- Skip assumptions.
- Skip UX risks.
- Make dashboards look like marketing pages.
- Make landing pages behave like dashboards.
- Overload the first screen with too much information.

---

## Example Trigger Phrases

Use this skill when the user says:

- “Run UX strategy for this brief.”
- “Create the UX flow.”
- “Plan the page structure.”
- “Create the information architecture.”
- “Define the user journey.”
- “Prepare UX strategy before design.”
- “Turn this client brief into UX strategy.”
- “What should the screen flow be?”
- “Create the layout logic before Stitch.”
- “Prepare the UX strategy document.”

---

## Example Lightweight Output

```md
# UX Strategy Document

## 1. Strategy Summary

**Client/Product:** UrbanNest Interiors  
**Project Type:** Premium interior design landing page  
**Primary User Outcome:** Understand the studio’s quality, trust the process, and book a consultation.  
**Primary Business Outcome:** Generate qualified consultation inquiries from premium homeowners.  
**Core UX Challenge:** Build trust quickly while creating a premium, aspirational experience.  
**Recommended UX Approach:** Use a conversion-focused landing page flow with strong portfolio proof, process clarity, testimonials, and repeated but restrained consultation CTAs.

---

## 2. UX Objective

**What The User Needs To Do:** Evaluate the studio and confidently book a consultation.  
**What The Business Needs To Achieve:** Capture qualified leads.  
**What The UI Must Make Easy:** View work, understand service quality, trust the team, and contact quickly.  
**What The UI Must Avoid:** Feeling generic, overcrowded, or unclear about next steps.

---

## 3. Primary User Journey

```txt
Step 1: Arrive and understand the premium interior design offer.
Step 2: View proof through portfolio and project highlights.
Step 3: Understand the process and service scope.
Step 4: Resolve doubts through testimonials and FAQs.
Step 5: Submit consultation request.
Final Action: Book a consultation.
```

---

## 4. Page / Screen Hierarchy

### Page/Screen 1: Landing Page

**Primary Goal:** Convert visitors into consultation inquiries.  
**Primary CTA:** Book a Consultation  
**Secondary CTA:** View Projects  
**User Questions Answered:** Is this studio premium? Can I trust them? Do they match my taste? What happens next?  
**Content Priority:** Promise, portfolio proof, process, testimonials, consultation CTA.

**Recommended Sections:**

1. Hero with premium value proposition and CTA
2. Featured project showcase
3. Service benefits
4. Design process
5. Testimonials / trust proof
6. FAQ
7. Final consultation CTA

**UX Notes:**

- Show visual proof early.
- Keep copy concise and premium.
- Repeat CTA after proof and near the footer.

---

## 6. Conversion Strategy

**Primary CTA:** Book a Consultation  
**Secondary CTA:** View Projects  
**CTA Placement Strategy:** Hero, after portfolio, after process, final CTA.  
**Lead Capture Strategy:** Short form with name, phone/email, property type, budget range, and preferred consultation time.  
**Trust-Building Elements:** Portfolio, testimonials, process, years of experience, client logos if available.  
**Objection Handling:** Address timeline, budget, quality, and execution reliability in FAQ.  
**Final Conversion Path:** Hero → Portfolio → Process → Testimonial → FAQ → Consultation form.

---

## 12. UX Risks

- Weak or stock imagery may reduce the premium feel.
- Too much copy may make the page feel heavy.
- If the consultation form is too long, conversion may drop.

---

## 14. Recommended Next Step

Run the **Design DNA Skill** using this UX Strategy Document.
```

---

## Project Memory Behavior

**Skill Number:** 02
**Skill Role:** UX Strategy — reads client brief, produces UX strategy document.

Before running this skill:

1. Check whether `.agency/` exists.
2. If `.agency/` does not exist, ask the user to run the Client Discovery Skill first, or create the `.agency/` structure from available context.
3. Read `.agency/CURRENT_CONTEXT.md` first.
4. Read `.agency/CONTEXT_INDEX.json` second.
5. Read only the required context files listed below.
6. Do not read every `.md` file by default.
7. Do not restart the project from zero.
8. Preserve previous decisions.

### Required Context Files For This Skill

- `.agency/CURRENT_CONTEXT.md`
- `.agency/CLIENT_BRIEF.md`
- `.agency/PROJECT_STATE.json`

### Skill Output Files

After completing this skill, write output to:

- `.agency/UX_STRATEGY.md` — the UX Strategy Document
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

1. Save the UX Strategy Document to `.agency/UX_STRATEGY.md`.
2. Update `.agency/CURRENT_CONTEXT.md` with current phase, completed items, and next step.
3. Update `.agency/PROJECT_STATE.json`.
4. Update `.agency/CONTEXT_INDEX.json`:
   - Set `current_phase` to `ux-strategy`
   - Set `current_skill` to `design-dna`
   - Set `required_context_files` to `[".agency/CURRENT_CONTEXT.md", ".agency/CLIENT_BRIEF.md", ".agency/UX_STRATEGY.md", ".agency/PROJECT_STATE.json"]`
5. Append a short entry to `.agency/CHANGELOG.md`.
6. Update `.agency/TODO.md` with next steps.
7. Add major UX decisions to `.agency/DECISIONS.md`.
8. Do not delete previous decisions or changelog entries.
