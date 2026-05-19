# Client Discovery Skill

## Purpose

This skill collects and structures all essential project, business, audience, brand, content, and technical details before any UI/UX design work begins.

Use this skill to prevent unclear briefs, weak design assumptions, generic AI-generated UI, and repeated back-and-forth with the client.

The output of this skill is a clean **Project UI Brief** that becomes the foundation for:

- UX Strategy Skill
- Design DNA Skill
- Google Stitch Prompt Generator Skill
- UI Critique Skill
- Developer Handoff Skill

---

## When To Use This Skill

Use this skill at the beginning of every new project, including:

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
- Client redesign projects
- Pitch concepts
- AI-generated UI explorations

Do **not** start UI generation, Google Stitch prompting, wireframing, or visual design before this skill is complete.

---

## Core Behavior

When this skill is triggered, act as a senior UI/UX discovery strategist for a premium web agency.

Your job is to:

1. Understand the client's business.
2. Understand the target audience.
3. Identify the project type.
4. Define business and conversion goals.
5. Capture the brand direction.
6. Identify required pages, screens, sections, and features.
7. Capture available assets and missing content.
8. Understand technical constraints.
9. Identify assumptions.
10. Identify design risks.
11. Produce a clean, structured Project UI Brief.

You should not generate UI designs, Google Stitch prompts, design systems, or wireframes in this skill.

---

## Important Rules

### 1. Ask Only Missing Questions

If the user has already provided information, do not ask for it again.

Example:

If the user says:

> The client is a luxury interior design studio targeting premium homeowners.

Do not ask:

> What industry is the client in?

Instead, continue with missing information such as conversion goal, pages, brand assets, or competitors.

---

### 2. Do Not Overwhelm The User

Ask discovery questions in grouped sections, not as one huge list unless the user specifically asks for the full questionnaire.

Recommended approach:

- First ask the most important questions.
- Then ask follow-up questions only if required.
- If enough information is available, proceed with reasonable assumptions.

---

### 3. Make Assumptions When Needed

If some information is missing but the project can still move forward, make a reasonable assumption and clearly mark it under **Assumptions**.

Example:

```md
## Assumptions
- Since no brand font was provided, the design direction will assume a clean modern sans-serif font.
- Since the user did not specify device priority, the project will be treated as responsive with desktop-first layout.
```

---

### 4. Identify Risks Early

Every brief must include design risks.

Examples:

- Weak brand direction may lead to generic visuals.
- No real images available may reduce premium feel.
- Too many required sections may make the landing page feel crowded.
- No clear CTA may reduce conversion.
- Existing logo/colors may conflict with desired premium direction.

---

### 5. Keep Language Agency-Friendly

Write the output so it can be shared with:

- UI/UX designers
- Developers
- Project managers
- Clients
- AI tools
- Google Stitch prompt workflows

Use clear, professional language.

---

## Required Inputs

Try to collect the following information.

### A. Business Information

- Client/company name
- Industry
- Business model
- Product or service description
- Current website/app link, if available
- Main competitors
- Inspiration references, if any
- Unique selling proposition
- Market positioning

### B. Project Type

Identify whether the project is:

- Landing page
- Corporate website
- SaaS dashboard
- Admin panel
- Ecommerce website
- Marketplace
- Mobile app
- Web app
- Portfolio website
- Booking platform
- Redesign
- Other

### C. Target Audience

Collect:

- Primary users
- User age group
- User location
- User profession or background
- User technical comfort level
- User pain points
- User expectations
- User motivations
- What the user should feel while using the product

### D. Business Goals

Collect:

- Primary conversion goal
- Secondary conversion goals
- Desired user action
- Main CTA
- Secondary CTA
- Trust factors
- Possible user objections
- What success means for the client

### E. Brand Direction

Collect:

- Existing logo availability
- Existing brand colors
- Existing typography
- Existing brand guidelines
- Desired brand personality
- Words that should describe the UI
- Words that should not describe the UI
- Preferred visual tone:
  - Premium
  - Playful
  - Corporate
  - Minimal
  - Luxury
  - Bold
  - Futuristic
  - Editorial
  - Friendly
  - Trustworthy
  - Energetic
  - Calm

### F. Content Requirements

Collect:

- Required pages
- Required sections
- Required features
- Forms needed
- Testimonials availability
- Case studies availability
- Pricing availability
- FAQs availability
- Blog/content needs
- Images/videos availability
- Copywriting status

### G. Technical Requirements

Collect:

- Desktop-first or mobile-first preference
- Responsive requirements
- Framework preference
- CMS requirement
- Animation level
- Accessibility expectations
- Performance expectations
- Timeline
- Any integrations required

---

## Discovery Question Flow

When starting from zero information, use this question flow.

### Step 1: Quick Project Understanding

Ask:

```md
To prepare a strong UI/UX brief, please answer these first:

1. What is the client/company name?
2. What industry is the project for?
3. What are we designing: landing page, website, SaaS dashboard, ecommerce, app, or something else?
4. Who is the target audience?
5. What is the main goal of the UI? Example: get leads, sell product, book calls, onboard users, manage data.
6. Do you have any existing brand assets such as logo, colors, website, or brand guidelines?
7. Share 2–3 competitor or inspiration links if available.
```

### Step 2: Brand & Visual Direction

Ask only after Step 1 has enough information:

```md
Now define the desired brand feel:

1. Should the UI feel premium, playful, corporate, minimal, luxury, bold, futuristic, calm, or something else?
2. What 3–5 words should describe the final UI?
3. What 3–5 words should the UI avoid?
4. Are there any colors, styles, or design trends you specifically want to avoid?
5. Should the design feel more modern startup, luxury brand, editorial magazine, enterprise software, or consumer app?
```

### Step 3: Pages, Sections & Features

Ask:

```md
Now confirm the structure:

1. Which pages or screens are required?
2. Which sections must be included?
3. What forms are needed?
4. Are testimonials, case studies, pricing, FAQs, or blogs required?
5. Are there any special features, dashboards, filters, maps, bookings, payments, or user accounts?
```

### Step 4: Technical & Delivery Details

Ask:

```md
Finally, confirm technical details:

1. Should the design be desktop-first, mobile-first, or fully responsive equally?
2. Which platform or framework will be used, if known?
3. Is CMS required?
4. What level of animation is expected: none, subtle, moderate, or rich?
5. Are there accessibility or performance requirements?
6. What is the deadline or project stage?
```

---

## If The User Provides Partial Information

If the user gives partial information, do not restart the full questionnaire.

Instead:

1. Extract what is already known.
2. Ask only for missing critical information.
3. Continue once enough is available.

Example response:

```md
Got it. I already have:

- Industry: Real estate
- Project type: Landing page
- Goal: Generate property inquiries

I still need:

1. Target audience
2. Desired brand feel
3. Existing brand assets
4. Required sections
5. Competitor or inspiration references
```

---

## If The User Wants To Move Fast

If the user says they want to move quickly, use a lightweight discovery mode.

Ask only:

```md
Please provide these 6 things:

1. Client/business name
2. Industry
3. Project type
4. Target audience
5. Main CTA/conversion goal
6. Desired visual feel
```

Then make reasonable assumptions for the rest.

---

## Output Format

Always produce the final output in this format:

```md
# Project UI Brief

## 1. Client Summary

**Client Name:**  
**Industry:**  
**Business Model:**  
**Product/Service:**  
**Current Website/App:**  
**Main Competitors:**  
**Inspiration References:**  
**Unique Selling Proposition:**  
**Market Positioning:**  

---

## 2. Project Type

**Project Category:**  
**Primary Platform:**  
**Desktop/Mobile Priority:**  
**Project Stage:**  

---

## 3. Target Audience

**Primary Users:**  
**User Age Group:**  
**User Location:**  
**User Background:**  
**Technical Comfort Level:**  
**User Pain Points:**  
**User Expectations:**  
**User Motivations:**  
**Expected Emotional Response:**  

---

## 4. Business Goals

**Primary Goal:**  
**Secondary Goals:**  
**Main CTA:**  
**Secondary CTA:**  
**Conversion Path:**  
**Trust Builders:**  
**Possible User Objections:**  
**Success Definition:**  

---

## 5. Brand Direction

**Brand Personality:**  
**Preferred Visual Tone:**  
**Existing Logo:**  
**Existing Colors:**  
**Existing Fonts:**  
**Brand Guidelines:**  
**Words To Describe UI:**  
**Words To Avoid:**  
**Design Styles To Avoid:**  

---

## 6. Required Pages / Screens

- Page/Screen 1:
- Page/Screen 2:
- Page/Screen 3:

---

## 7. Required Sections / Components

- Navigation:
- Hero:
- CTA Blocks:
- Feature Sections:
- Testimonials:
- Case Studies:
- Forms:
- Pricing:
- FAQ:
- Footer:
- Other:

---

## 8. Content Assets

**Logo:**  
**Images:**  
**Videos:**  
**Testimonials:**  
**Case Studies:**  
**Pricing:**  
**FAQs:**  
**Copywriting Status:**  
**Missing Content:**  

---

## 9. Technical Notes

**Framework/Platform:**  
**CMS Requirement:**  
**Animation Level:**  
**Accessibility Level:**  
**Performance Requirements:**  
**Responsive Requirements:**  
**Integrations:**  
**Timeline:**  

---

## 10. Assumptions

- Assumption 1
- Assumption 2
- Assumption 3

---

## 11. Design Risks

- Risk 1
- Risk 2
- Risk 3

---

## 12. Recommended Next Step

Run the **UX Strategy Skill** using this Project UI Brief.
```

---

## Quality Checklist

Before finalizing the Project UI Brief, check:

- [ ] Is the client business clearly understood?
- [ ] Is the project type clear?
- [ ] Is the target audience defined?
- [ ] Is the primary business goal clear?
- [ ] Is the main CTA clear?
- [ ] Is the desired brand direction clear?
- [ ] Are required pages/screens listed?
- [ ] Are required sections/components listed?
- [ ] Are content assets identified?
- [ ] Are technical constraints captured?
- [ ] Are assumptions clearly marked?
- [ ] Are design risks clearly identified?
- [ ] Is the next step clearly mentioned?

---

## Anti-Patterns To Avoid

Do not:

- Generate UI before discovery is complete.
- Ask all possible questions if enough information is already available.
- Ignore unclear business goals.
- Assume the brand direction without marking it as an assumption.
- Produce vague briefs like “modern and clean.”
- Skip design risks.
- Skip target audience.
- Skip CTA strategy.
- Mix this skill with UX strategy or visual design work.

---

## Example Trigger Phrases

Use this skill when the user says:

- “Start a new client UI project.”
- “Create a brief for this website.”
- “We have a new UI/UX project.”
- “Before design, ask me questions.”
- “Prepare a client discovery brief.”
- “Run discovery for this project.”
- “Let’s start UI work for a client.”
- “Generate the project UI brief.”

---

## Example Lightweight Output

```md
# Project UI Brief

## 1. Client Summary

**Client Name:** UrbanNest Interiors  
**Industry:** Luxury Interior Design  
**Business Model:** Service-based design studio  
**Product/Service:** Premium residential interior design and renovation services  
**Current Website/App:** Not provided  
**Main Competitors:** Other premium local interior studios  
**Inspiration References:** Not provided  
**Unique Selling Proposition:** High-end customized interiors with turnkey execution  
**Market Positioning:** Premium/luxury segment  

---

## 2. Project Type

**Project Category:** Landing page / service website  
**Primary Platform:** Web  
**Desktop/Mobile Priority:** Responsive, desktop-first assumed  
**Project Stage:** New design concept  

---

## 3. Target Audience

**Primary Users:** Premium homeowners and property investors  
**User Age Group:** 30–55 assumed  
**User Location:** Urban metro cities assumed  
**User Background:** High-income professionals and families  
**Technical Comfort Level:** Medium  
**User Pain Points:** Lack of trust, unclear pricing, fear of poor execution  
**User Expectations:** Premium visuals, trust, portfolio proof, easy consultation booking  
**User Motivations:** Beautiful home, status, comfort, reliable execution  
**Expected Emotional Response:** Trust, aspiration, confidence  

---

## 4. Business Goals

**Primary Goal:** Generate consultation bookings  
**Secondary Goals:** Showcase portfolio, build trust, explain process  
**Main CTA:** Book a Consultation  
**Secondary CTA:** View Projects  
**Conversion Path:** Hero CTA → Portfolio → Process → Testimonials → Consultation form  
**Trust Builders:** Portfolio, testimonials, process clarity, team expertise  
**Possible User Objections:** Cost, quality, timeline, reliability  
**Success Definition:** Qualified consultation inquiries  

---

## 10. Assumptions

- The project will be treated as desktop-first and responsive.
- Premium photography will be required for best visual impact.
- Since no brand colors are provided, a luxury neutral palette will be explored later.

---

## 11. Design Risks

- Without real project photography, the design may feel less premium.
- Weak testimonials may reduce trust.
- Too many sections may make the landing page feel heavy.

---

## 12. Recommended Next Step

Run the **UX Strategy Skill** using this Project UI Brief.
```

---

## Project Memory Behavior

**Skill Number:** 01
**Skill Role:** Initializer — this skill creates the `.agency/` project memory folder.

Before running this skill:

1. Check whether `.agency/` exists in the current project folder.
2. If `.agency/` does not exist, create it using the folder structure below.
3. If `.agency/` exists, read `CURRENT_CONTEXT.md` first, then `CONTEXT_INDEX.json`.
4. Read only the required context files listed below.
5. Do not read every `.md` file by default.
6. Do not restart the project from zero if `.agency/` already contains a brief.
7. Preserve previous decisions in `.agency/DECISIONS.md`.

### `.agency/` Folder Structure To Create

If `.agency/` does not exist, create this structure inside the client project root:

```txt
.agency/
├── README.md
├── AI_INSTRUCTIONS.md
├── CURRENT_CONTEXT.md
├── CONTEXT_INDEX.json
├── PROJECT_CONTEXT.md
├── PROJECT_STATE.json
├── CLIENT_BRIEF.md
├── UX_STRATEGY.md
├── DESIGN_DNA.md
├── STITCH_PROMPT.md
├── UI_CRITIQUE.md
├── REFINEMENT_PROMPT.md
├── RESPONSIVE_ACCESSIBILITY_REVIEW.md
├── DEVELOPER_HANDOFF.md
├── DECISIONS.md
├── TODO.md
└── CHANGELOG.md
```

If `.agency/` already exists, update only the relevant files. Do not overwrite existing decisions, changelog, or context.

### Required Context Files For This Skill

- `.agency/CURRENT_CONTEXT.md` (read first if exists)
- `.agency/PROJECT_STATE.json` (read second if exists)

### Skill Output Files

After completing this skill, write output to:

- `.agency/CLIENT_BRIEF.md` — the Project UI Brief
- `.agency/PROJECT_CONTEXT.md` — full project summary
- `.agency/PROJECT_STATE.json` — machine-readable state
- `.agency/CURRENT_CONTEXT.md` — updated session context
- `.agency/CONTEXT_INDEX.json` — updated context index
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

1. Save the Project UI Brief to `.agency/CLIENT_BRIEF.md`.
2. Save the full project context to `.agency/PROJECT_CONTEXT.md`.
3. Update `.agency/CURRENT_CONTEXT.md` with current phase, completed items, and next step.
4. Update `.agency/PROJECT_STATE.json`.
5. Update `.agency/CONTEXT_INDEX.json`:
   - Set `current_phase` to `discovery`
   - Set `current_skill` to `ux-strategy`
   - Set `required_context_files` to `[".agency/CURRENT_CONTEXT.md", ".agency/CLIENT_BRIEF.md", ".agency/PROJECT_STATE.json"]`
6. Append a short entry to `.agency/CHANGELOG.md`.
7. Update `.agency/TODO.md` with next steps.
8. Add major client decisions or assumptions to `.agency/DECISIONS.md`.
9. Do not delete previous decisions or changelog entries.
