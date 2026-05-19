# Responsive + Accessibility Review Skill

## Purpose

This skill reviews a selected UI concept for responsive behavior, accessibility basics, usability, interaction clarity, and implementation readiness before developer handoff.

The goal is to identify practical issues that may not be visible in a beautiful desktop concept, especially problems related to mobile layout, contrast, touch targets, forms, navigation, content stacking, and accessibility.

The output of this skill is a **Responsive + Accessibility Review Report** that becomes the foundation for:

- Final UI refinement
- Developer Handoff Skill
- QA checklist
- Implementation planning
- Client approval notes

---

## When To Use This Skill

Use this skill after:

1. A final or near-final UI concept has been selected.
2. The UI Critique Skill has been completed.
3. The Humanization & Refinement Skill has improved the concept.
4. The team is preparing for development or final approval.

Use it for:

- Landing pages
- Corporate websites
- SaaS dashboards
- Admin panels
- Ecommerce websites
- Marketplaces
- Mobile apps
- Web apps
- Portfolio websites
- Booking platforms
- Forms
- Checkout flows
- Dashboards
- Data-heavy interfaces

Do **not** use this skill as the first design review.

This skill is specifically for **responsive, accessibility, usability, and implementation-readiness checks**.

---

## Core Behavior

When this skill is triggered, act as a senior UI/UX QA reviewer, accessibility-conscious product designer, and frontend implementation advisor.

Your job is to:

1. Review desktop layout readiness.
2. Review tablet behavior.
3. Review mobile behavior.
4. Review navigation behavior across devices.
5. Review CTA visibility across devices.
6. Review content stacking.
7. Review forms and inputs.
8. Review tables, cards, charts, and complex modules.
9. Review accessibility basics.
10. Review interaction states.
11. Review implementation risks.
12. Produce a clear Responsive + Accessibility Review Report.

Be practical and implementation-focused.

---

## Required Input

This skill works best with:

- Final UI screenshot or design concept
- Desktop version
- Mobile version, if available
- Tablet version, if available
- Design DNA Document
- UX Strategy Document
- UI Critique Report
- Humanization & Refinement Plan
- Target platform/framework, if known

Minimum required input:

- UI screenshot or design description
- Project type
- Target devices

If mobile/tablet versions are missing, infer likely responsive behavior and clearly mark those sections as assumptions.

---

## Important Rules

### 1. Do Not Only Judge Beauty

A UI can look beautiful and still fail on mobile or accessibility.

Always review:

- Can users read it?
- Can users tap it?
- Can users navigate it?
- Can users complete the task?
- Can developers build it consistently?
- Does it work when content changes?

---

### 2. Check Mobile Early

Many AI-generated desktop designs break on mobile.

Look for:

- Too many columns
- Complex hero layouts
- Tiny text
- Overcrowded cards
- Tables that cannot fit
- Large decorative visuals
- Hidden CTAs
- Long forms
- Weak navigation
- Content order problems

---

### 3. Accessibility Review Is Practical, Not Legal Certification

This skill does not provide formal legal accessibility certification.

It should identify practical accessibility risks such as:

- Low contrast
- Tiny text
- Missing focus states
- Weak form labels
- Color-only status communication
- Small tap targets
- Overuse of motion
- Ambiguous buttons
- Poor reading order

---

### 4. Review Touch Targets

For mobile and tablet, ensure tappable elements are large enough and spaced well.

Check:

- Buttons
- Icon buttons
- Form fields
- Menu items
- Tabs
- Dropdowns
- Cards
- Filters
- Pagination
- Date pickers
- Sliders

---

### 5. Review Forms Carefully

Forms are conversion-critical.

Check:

- Label clarity
- Required/optional fields
- Error messages
- Success states
- Focus states
- Input sizing
- Mobile keyboard behavior
- Field grouping
- Form length
- Submit button visibility

---

### 6. Review Navigation Behavior

Navigation should adapt by project type.

Landing page:

- Mobile menu should be simple.
- CTA should remain visible or easy to reach.

Dashboard:

- Sidebar should collapse or become bottom navigation/drawer.
- Search and key actions should remain accessible.

Ecommerce:

- Search, cart, filters, and categories should be easy to reach.

Mobile app:

- Bottom navigation should be thumb-friendly.

---

### 7. Review Complex Components

For dashboards, admin panels, and ecommerce, check:

- Tables
- Filters
- Charts
- Cards
- Data lists
- Detail drawers
- Modals
- Product grids
- Checkout flows

Ask:

- What happens on mobile?
- Does it become cards?
- Does it scroll horizontally?
- Is the priority information still visible?
- Are actions accessible?

---

### 8. Include Developer Notes

Every report should include practical notes developers can use.

Examples:

- Collapse 4-column feature grid into 1 column below 768px.
- Convert data table into stacked cards on mobile.
- Keep primary CTA sticky on mobile for long landing pages.
- Use visible focus ring for keyboard navigation.
- Disable large reveal animations for reduced-motion preference.

---

## Review Process

Follow this process every time:

### Step 1: Identify Review Context

Determine:

- Project type
- Screen/page
- Target devices
- Main user action
- Framework/CMS, if known
- Whether mobile/tablet designs exist

### Step 2: Desktop Review

Check:

- Layout clarity
- Grid consistency
- CTA visibility
- Content hierarchy
- Section spacing
- Component consistency
- Above-the-fold clarity

### Step 3: Tablet Review

Check:

- Two-column to one-column transitions
- Navigation behavior
- Card wrapping
- Image cropping
- CTA positioning
- Form width
- Section spacing

### Step 4: Mobile Review

Check:

- Content stacking order
- Navigation
- CTA visibility
- Tap target size
- Text size
- Form usability
- Image behavior
- Scroll length
- Sticky elements
- Performance-heavy visuals

### Step 5: Accessibility Review

Check:

- Contrast
- Text size
- Touch targets
- Keyboard focus
- Form labels
- Error messages
- Color-only status
- Motion sensitivity
- Alt text needs
- Semantic structure

### Step 6: Interaction States Review

Check:

- Hover states
- Focus states
- Active states
- Loading states
- Empty states
- Error states
- Success states
- Disabled states

### Step 7: Implementation Risk Review

Check:

- Hard-to-build layouts
- Inconsistent component rules
- Overly complex animations
- Undefined responsive behavior
- CMS/content flexibility issues
- Unclear assets
- Missing states
- Performance risks

### Step 8: Produce Final Report

Use the output format below.

---

## Output Format

Always produce the final output in this format:

```md
# Responsive + Accessibility Review Report

## 1. Review Context

**Client/Product:**  
**Screen/Page Reviewed:**  
**Project Type:**  
**Primary User Action:**  
**Target Devices:**  
**Framework/CMS:**  
**Review Limitation:**  

---

## 2. Overall Readiness

**Readiness Status:** Ready / Needs Minor Fixes / Needs Major Fixes / Not Ready  
**Overall Score:** /10

### Score Breakdown

| Criteria | Score | Notes |
|---|---:|---|
| Desktop Readiness | /10 |  |
| Tablet Readiness | /10 |  |
| Mobile Readiness | /10 |  |
| Accessibility Basics | /10 |  |
| Interaction States | /10 |  |
| Form Usability | /10 |  |
| Navigation Behavior | /10 |  |
| Implementation Readiness | /10 |  |

---

## 3. Desktop Review

**Assessment:**  

**Strengths:**  
- 
- 
- 

**Issues:**  
- 
- 
- 

**Recommended Fixes:**  
- 
- 
- 

---

## 4. Tablet Review

**Expected Behavior:**  

**Issues:**  
- 
- 
- 

**Recommended Fixes:**  
- 
- 
- 

---

## 5. Mobile Review

**Expected Behavior:**  

**Mobile Content Priority:**  
1. 
2. 
3. 
4. 

**Issues:**  
- 
- 
- 

**Recommended Fixes:**  
- 
- 
- 

---

## 6. Navigation Review

**Desktop Navigation:**  
**Tablet Navigation:**  
**Mobile Navigation:**  

**Issues:**  
- 
- 
- 

**Recommended Fixes:**  
- 
- 
- 

---

## 7. CTA Review

**Primary CTA:**  
**CTA Visibility On Desktop:**  
**CTA Visibility On Mobile:**  
**CTA Placement Issues:**  

**Recommended Fixes:**  
- 
- 
- 

---

## 8. Forms Review

**Forms Present:** Yes / No  
**Form Purpose:**  

**Issues:**  
- 
- 
- 

**Recommended Fixes:**  
- 
- 
- 

**Required Form States:**  
- Default
- Focus
- Error
- Success
- Loading
- Disabled

---

## 9. Complex Components Review

Use this section for dashboards, ecommerce, admin panels, tables, charts, filters, maps, or product grids.

**Components Reviewed:**  
- 

**Responsive Concerns:**  
- 
- 
- 

**Recommended Fixes:**  
- 
- 
- 

---

## 10. Accessibility Review

**Contrast:**  
**Text Size:**  
**Touch Targets:**  
**Keyboard Navigation:**  
**Focus States:**  
**Form Labels:**  
**Error Messages:**  
**Color-Blind Safety:**  
**Motion Sensitivity:**  
**Alt Text Needs:**  
**Semantic Structure:**  

**Accessibility Issues:**  
- 
- 
- 

**Recommended Fixes:**  
- 
- 
- 

---

## 11. Interaction States Review

**Hover States:**  
**Focus States:**  
**Active States:**  
**Loading States:**  
**Empty States:**  
**Error States:**  
**Success States:**  
**Disabled States:**  

**Missing States:**  
- 
- 
- 

---

## 12. Performance & Practicality Notes

**Heavy Visual Risks:**  
**Animation Risks:**  
**Image/Video Risks:**  
**CMS Content Risks:**  
**Scalability Risks:**  

**Recommended Fixes:**  
- 
- 
- 

---

## 13. Developer Responsive Rules

- 
- 
- 
- 
- 

---

## 14. Must-Fix Before Development

1. 
2. 
3. 
4. 
5. 

---

## 15. Nice-To-Have Improvements

- 
- 
- 

---

## 16. Final Recommendation

**Decision:** Approve / Approve With Fixes / Revise Before Handoff / Redesign Required  

**Reason:**  

---

## 17. Recommended Next Step

Run the **Developer Handoff Skill** after the must-fix items are resolved.
```

---

## Readiness Status Guide

### Ready

Use when:

- Desktop, tablet, and mobile behavior are clear.
- Accessibility basics are acceptable.
- Interactions and states are mostly defined.
- Developer can proceed confidently.

### Needs Minor Fixes

Use when:

- UI is mostly ready.
- Some responsive, accessibility, or state details need clarification.
- Issues are not blocking major development.

### Needs Major Fixes

Use when:

- Mobile layout is unclear or weak.
- CTA/form/navigation issues may hurt conversion.
- Accessibility basics are weak.
- Important states are missing.

### Not Ready

Use when:

- Concept is visually attractive but impractical.
- Mobile behavior is not feasible.
- Major UX flows are undefined.
- Developer would need to guess too much.

---

## Responsive Rules By Project Type

### A. Landing Page

Check:

- Hero headline remains readable on mobile.
- CTA appears early on mobile.
- Multi-column sections stack correctly.
- Trust strip does not overflow.
- Testimonials are easy to swipe or stack.
- FAQ is easy to tap.
- Contact form is short and usable.

Recommended mobile behavior:

```txt
Hero → Primary CTA → Trust proof → Main value → Visual proof → CTA → Details → FAQ → Final CTA
```

---

### B. SaaS Dashboard

Check:

- Sidebar collapses.
- Top search remains accessible.
- Metrics do not become too tiny.
- Tables become cards or scroll carefully.
- Charts remain readable.
- Priority actions remain visible.
- Empty/loading/error states exist.

Recommended mobile behavior:

```txt
Top summary → Priority alerts → Main action → Key modules → Recent activity
```

---

### C. Admin Panel

Check:

- Filters are usable on mobile.
- Tables transform into cards or focused lists.
- Bulk actions remain accessible.
- Status tags remain clear.
- Detail panels become full-screen drawers.
- Destructive actions require confirmation.

Recommended mobile behavior:

```txt
Search/filter → Status summary → List cards → Detail view → Action confirmation
```

---

### D. Ecommerce

Check:

- Product cards remain scannable.
- Price and CTA are visible.
- Filters open in drawer.
- Cart is always easy to reach.
- Product images crop safely.
- Reviews and shipping info are accessible.
- Checkout form is mobile-friendly.

Recommended mobile behavior:

```txt
Search/category → Filters drawer → Product list → Product detail → Sticky add-to-cart → Checkout
```

---

### E. Mobile App

Check:

- Bottom navigation is clear.
- Primary action is thumb-friendly.
- Text is not dense.
- Cards are readable.
- Forms minimize typing.
- Feedback states are clear.
- App can be used one-handed.

---

## Accessibility Basics Checklist

Use this checklist for every review:

- [ ] Body text is readable.
- [ ] Important text has sufficient contrast.
- [ ] Buttons are large enough to tap.
- [ ] Links are visually distinguishable.
- [ ] Form fields have visible labels.
- [ ] Error messages explain what went wrong.
- [ ] Focus states are visible.
- [ ] UI does not rely only on color to communicate status.
- [ ] Motion is not excessive.
- [ ] Reduced-motion alternative is considered.
- [ ] Images need alt text.
- [ ] Heading hierarchy is logical.
- [ ] Icons have labels or accessible names where needed.
- [ ] Disabled states are clear.
- [ ] Loading states are understandable.

---

## Common Issues And Fixes

### Issue: Four-Column Layout Breaks On Mobile

Fix:

```md
Use 4 columns on large desktop, 2 columns on tablet, and 1 column on mobile.
```

### Issue: CTA Disappears Below Fold On Mobile

Fix:

```md
Move primary CTA higher on mobile or add a sticky bottom CTA for long pages.
```

### Issue: Dashboard Table Too Wide

Fix:

```md
Convert table rows into stacked mobile cards with the most important fields visible first.
```

### Issue: Low-Contrast Text

Fix:

```md
Increase text contrast and avoid using low-opacity grey for body copy.
```

### Issue: Form Too Long

Fix:

```md
Group fields, remove unnecessary inputs, or split the form into steps if needed.
```

### Issue: Icon-Only Buttons Are Ambiguous

Fix:

```md
Add visible labels or accessible names. Use tooltips only as a secondary aid.
```

### Issue: Motion Too Heavy

Fix:

```md
Reduce animation duration, avoid parallax on mobile, and respect reduced-motion preferences.
```

### Issue: Cards Too Dense On Mobile

Fix:

```md
Prioritize title, key info, and action. Hide or collapse secondary metadata.
```

---

## Developer Responsive Rule Examples

Use rules like:

```md
- Use max-width container of 1200px on desktop with 24px horizontal padding on tablet and 16px on mobile.
- Collapse 3-column grids into 1 column below 768px.
- Convert sidebar navigation into drawer navigation below 1024px.
- Keep primary CTA visible in hero and repeat after major proof sections.
- Convert pricing cards into stacked cards on mobile.
- Convert data tables into card lists below 768px.
- Ensure all interactive elements have visible focus states.
- Use reduced-motion media query for reveal animations.
- Maintain minimum 44px tap target height for mobile controls.
```

---

## Quality Checklist

Before finalizing the report, check:

- [ ] Is the readiness status clear?
- [ ] Are desktop issues reviewed?
- [ ] Are tablet assumptions reviewed?
- [ ] Are mobile issues reviewed?
- [ ] Is CTA visibility reviewed?
- [ ] Is navigation reviewed?
- [ ] Are forms reviewed if present?
- [ ] Are complex components reviewed if present?
- [ ] Are accessibility basics checked?
- [ ] Are interaction states checked?
- [ ] Are developer responsive rules included?
- [ ] Are must-fix items listed?
- [ ] Is the final recommendation clear?
- [ ] Is the next step clearly mentioned?

---

## Anti-Patterns To Avoid

Do not:

- Approve a design just because it looks good on desktop.
- Ignore mobile behavior.
- Ignore forms.
- Ignore focus states.
- Ignore contrast.
- Ignore touch target size.
- Ignore content stacking.
- Ignore long text and real content.
- Ignore dashboard/table behavior.
- Ignore implementation practicality.
- Claim legal accessibility compliance.
- Give vague advice like “make it responsive.”
- Skip developer rules.

---

## Example Trigger Phrases

Use this skill when the user says:

- “Review responsiveness.”
- “Check mobile readiness.”
- “Check accessibility.”
- “Is this ready for development?”
- “Review before handoff.”
- “Check this UI for responsive issues.”
- “Find mobile problems.”
- “Check the design for accessibility.”
- “Prepare responsive QA.”
- “Can developers build this?”

---

## Example Output

```md
# Responsive + Accessibility Review Report

## 1. Review Context

**Client/Product:** UrbanNest Interiors  
**Screen/Page Reviewed:** Landing Page  
**Project Type:** Premium service website  
**Primary User Action:** Book a consultation  
**Target Devices:** Desktop-first responsive  
**Framework/CMS:** Not specified  
**Review Limitation:** Mobile version not provided; mobile behavior inferred from desktop concept.

---

## 2. Overall Readiness

**Readiness Status:** Needs Minor Fixes  
**Overall Score:** 7.8/10

### Score Breakdown

| Criteria | Score | Notes |
|---|---:|---|
| Desktop Readiness | 8.5/10 | Strong layout and hierarchy |
| Tablet Readiness | 7.5/10 | Needs clear grid collapse rules |
| Mobile Readiness | 7/10 | CTA and image stacking need definition |
| Accessibility Basics | 7/10 | Contrast likely okay, focus states missing |
| Interaction States | 6.5/10 | Loading/success/error states not defined |
| Form Usability | 7/10 | Consultation form should be shortened |
| Navigation Behavior | 8/10 | Simple nav should adapt well |
| Implementation Readiness | 7.5/10 | Needs responsive rules before handoff |

---

## 5. Mobile Review

**Expected Behavior:**  
Hero should stack with text first, CTA second, trust proof third, and image fourth or below the fold depending on visual priority.

**Mobile Content Priority:**  
1. Clear headline  
2. Book Consultation CTA  
3. Trust proof  
4. Featured project image  

**Issues:**  
- Hero image may push CTA too low on mobile.
- Feature cards need single-column stacking.
- Final consultation form may feel long on mobile.

**Recommended Fixes:**  
- Keep primary CTA visible within the first mobile viewport.
- Collapse all multi-column sections to one column below 768px.
- Use a shorter consultation form or split optional fields.

---

## 10. Accessibility Review

**Contrast:** Mostly acceptable, but muted text should be checked.  
**Text Size:** Body text should not go below 16px on mobile.  
**Touch Targets:** Buttons and nav items should be at least 44px tall.  
**Keyboard Navigation:** Focus states need to be defined.  
**Form Labels:** Labels should remain visible, not only placeholders.  
**Error Messages:** Need clear validation messages.  
**Color-Blind Safety:** Do not rely only on color for form errors.  
**Motion Sensitivity:** Reveal animations should respect reduced-motion settings.  
**Alt Text Needs:** Project images need descriptive alt text.  
**Semantic Structure:** Use one H1 and logical H2/H3 hierarchy.

---

## 13. Developer Responsive Rules

- Use 12-column desktop grid, 6-column tablet grid, and 1-column mobile stack.
- Collapse project cards into one-column layout below 768px.
- Keep primary CTA visible in the hero on mobile.
- Use 16px horizontal padding on mobile.
- Ensure all buttons have minimum 44px tap height.
- Add visible focus states for links, buttons, and form fields.
- Use real form labels instead of placeholder-only labels.
- Respect reduced-motion preferences for reveal animations.

---

## 14. Must-Fix Before Development

1. Define mobile hero stacking order.
2. Define consultation form mobile behavior.
3. Add focus states.
4. Confirm contrast for muted text.
5. Define success/error states for form submission.

---

## 16. Final Recommendation

**Decision:** Approve With Fixes  

**Reason:** The concept is visually strong and mostly practical, but responsive behavior and accessibility states need definition before developer handoff.

---

## 17. Recommended Next Step

Run the **Developer Handoff Skill** after the must-fix items are resolved.
```

---

## Project Memory Behavior

**Skill Number:** 07
**Skill Role:** Responsive + Accessibility Review — checks final UI for responsive behavior and accessibility before handoff.

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
- `.agency/PROJECT_STATE.json`

### Skill Output Files

After completing this skill, write output to:

- `.agency/RESPONSIVE_ACCESSIBILITY_REVIEW.md` — the Responsive + Accessibility Review Report
- `.agency/PROJECT_STATE.json` — updated state
- `.agency/CURRENT_CONTEXT.md` — updated session context
- `.agency/CONTEXT_INDEX.json` — updated index
- `.agency/CHANGELOG.md` — append entry
- `.agency/TODO.md` — update must-fix items

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

1. Save the Review Report to `.agency/RESPONSIVE_ACCESSIBILITY_REVIEW.md`.
2. Update `.agency/CURRENT_CONTEXT.md` with current phase, completed items, and next step.
3. Update `.agency/PROJECT_STATE.json`.
4. Update `.agency/CONTEXT_INDEX.json`:
   - Set `current_phase` to `responsive-review`
   - Set `current_skill` to `developer-handoff`
   - Set `required_context_files` to `[".agency/CURRENT_CONTEXT.md", ".agency/DESIGN_DNA.md", ".agency/RESPONSIVE_ACCESSIBILITY_REVIEW.md"]`
5. Append a short entry to `.agency/CHANGELOG.md`.
6. Update `.agency/TODO.md` with must-fix items before development.
7. Add any accessibility or responsive decisions to `.agency/DECISIONS.md`.
8. Do not delete previous decisions or changelog entries.
