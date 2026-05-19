---
skill_id: uiux-design-system-export
skill_number: 08.5
requires_visual_input: false
requires_browser: false
project_complexity: standard, full
human_checkpoint_after: false
output_files:
  - .agency/DESIGN_SYSTEM.css
  - .agency/DESIGN_SYSTEM_TOKENS.json
reads_from:
  - .agency/DESIGN_DNA.md
  - .agency/DEVELOPER_HANDOFF.md
---

# Design System Export Skill

## Purpose

This skill converts the Design DNA and Developer Handoff into production-ready design system files:

1. **`DESIGN_SYSTEM.css`** — CSS custom properties ready to paste into any project
2. **`DESIGN_SYSTEM_TOKENS.json`** — Design tokens in W3C token format, importable into Figma, Style Dictionary, Theo, or any design token tooling

Use this skill after Developer Handoff. Before development begins.

---

## When To Use

- After Developer Handoff is complete
- Before developer starts coding
- When designer needs to import tokens into Figma
- When team uses Style Dictionary or design token pipeline
- When client project uses Tailwind, and config needs to match design
- For any project where design consistency must be enforced in code

Skip for lite projects. Mark `design_system_export.status` as `skipped` in `PROJECT_STATE.json`.

---

## Core Behavior

When triggered:

1. Read `DESIGN_DNA.md` — extract all visual values (colors, typography, spacing, radius, shadow, motion).
2. Read `DEVELOPER_HANDOFF.md` — extract component-level tokens (button sizes, input heights, card radius, etc.).
3. Generate CSS custom properties from all extracted values.
4. Generate W3C-format design token JSON from same values.
5. Generate Tailwind config extension block.
6. Validate: every token used in DEVELOPER_HANDOFF must exist in the output files.

---

## Token Naming Convention

All tokens use a two-level naming scheme:

```
--[category]-[variant]
```

Examples:
```css
--color-primary-500
--color-neutral-100
--font-size-heading-xl
--space-4
--radius-card
--shadow-card
--motion-duration-fast
```

Never use:
- `--btn-blue` (semantic not structural)
- `--color1` (meaningless)
- `--primary` (missing category prefix)

---

## Token Categories

### Colors

Generate a full scale for each palette color:

```css
/* Primary palette — 9-step scale */
--color-primary-50:  [lightest];
--color-primary-100: [light];
--color-primary-200: [soft];
--color-primary-300: [tint];
--color-primary-400: [mid-light];
--color-primary-500: [base];       /* main brand color */
--color-primary-600: [mid-dark];
--color-primary-700: [dark];
--color-primary-800: [darker];
--color-primary-900: [darkest];

/* Neutral palette */
--color-neutral-0:   #ffffff;
--color-neutral-50:  [near-white];
...
--color-neutral-950: [near-black];

/* Semantic tokens — reference palette tokens */
--color-bg-primary:   var(--color-neutral-0);
--color-bg-surface:   var(--color-neutral-50);
--color-text-primary: var(--color-neutral-900);
--color-text-muted:   var(--color-neutral-500);
--color-border:       var(--color-neutral-200);
--color-accent:       var(--color-primary-500);
--color-error:        #dc2626;
--color-success:      #16a34a;
--color-warning:      #d97706;
```

### Typography

```css
/* Font families */
--font-heading: '[Font Name]', sans-serif;
--font-body:    '[Font Name]', sans-serif;
--font-mono:    '[Font Name]', monospace;

/* Font sizes — T-shirt scale */
--font-size-xs:   0.75rem;   /* 12px */
--font-size-sm:   0.875rem;  /* 14px */
--font-size-base: 1rem;      /* 16px */
--font-size-md:   1.125rem;  /* 18px */
--font-size-lg:   1.25rem;   /* 20px */
--font-size-xl:   1.5rem;    /* 24px */
--font-size-2xl:  1.875rem;  /* 30px */
--font-size-3xl:  2.25rem;   /* 36px */
--font-size-4xl:  3rem;      /* 48px */
--font-size-5xl:  3.75rem;   /* 60px */

/* Font weights */
--font-weight-regular:  400;
--font-weight-medium:   500;
--font-weight-semibold: 600;
--font-weight-bold:     700;

/* Line heights */
--line-height-tight:  1.2;
--line-height-snug:   1.35;
--line-height-normal: 1.5;
--line-height-relaxed: 1.75;

/* Letter spacing */
--letter-spacing-tight:  -0.025em;
--letter-spacing-normal:  0;
--letter-spacing-wide:    0.025em;
--letter-spacing-wider:   0.05em;
--letter-spacing-widest:  0.1em;
```

### Spacing

Generate a consistent 4px base-unit scale:

```css
--space-0:   0;
--space-1:   0.25rem;  /* 4px */
--space-2:   0.5rem;   /* 8px */
--space-3:   0.75rem;  /* 12px */
--space-4:   1rem;     /* 16px */
--space-5:   1.25rem;  /* 20px */
--space-6:   1.5rem;   /* 24px */
--space-8:   2rem;     /* 32px */
--space-10:  2.5rem;   /* 40px */
--space-12:  3rem;     /* 48px */
--space-16:  4rem;     /* 64px */
--space-20:  5rem;     /* 80px */
--space-24:  6rem;     /* 96px */
--space-32:  8rem;     /* 128px */
```

### Border Radius

```css
--radius-none:   0;
--radius-sm:     0.25rem;  /* 4px */
--radius-base:   0.5rem;   /* 8px */
--radius-md:     0.75rem;  /* 12px */
--radius-lg:     1rem;     /* 16px */
--radius-xl:     1.5rem;   /* 24px */
--radius-2xl:    2rem;     /* 32px */
--radius-full:   9999px;
--radius-card:   var(--radius-lg);   /* semantic */
--radius-button: var(--radius-base); /* semantic */
--radius-input:  var(--radius-base); /* semantic */
--radius-badge:  var(--radius-full); /* semantic */
```

### Shadows

```css
--shadow-sm:   0 1px 2px 0 rgb(0 0 0 / 0.05);
--shadow-base: 0 1px 3px 0 rgb(0 0 0 / 0.1), 0 1px 2px -1px rgb(0 0 0 / 0.1);
--shadow-md:   0 4px 6px -1px rgb(0 0 0 / 0.1), 0 2px 4px -2px rgb(0 0 0 / 0.1);
--shadow-lg:   0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1);
--shadow-xl:   0 20px 25px -5px rgb(0 0 0 / 0.1), 0 8px 10px -6px rgb(0 0 0 / 0.1);
--shadow-card: var(--shadow-md);
--shadow-nav:  var(--shadow-sm);
--shadow-modal: var(--shadow-xl);
```

### Motion

```css
--motion-duration-instant: 0ms;
--motion-duration-fast:    150ms;
--motion-duration-base:    250ms;
--motion-duration-slow:    400ms;
--motion-duration-slower:  600ms;

--motion-easing-linear:    linear;
--motion-easing-in:        cubic-bezier(0.4, 0, 1, 1);
--motion-easing-out:       cubic-bezier(0, 0, 0.2, 1);
--motion-easing-in-out:    cubic-bezier(0.4, 0, 0.2, 1);
--motion-easing-bounce:    cubic-bezier(0.34, 1.56, 0.64, 1);
```

### Breakpoints

```css
--breakpoint-sm:  640px;
--breakpoint-md:  768px;
--breakpoint-lg:  1024px;
--breakpoint-xl:  1280px;
--breakpoint-2xl: 1536px;
```

### Layout

```css
--container-max:    1280px;
--container-prose:  65ch;
--grid-columns:     12;
--z-below:         -1;
--z-base:           0;
--z-raised:        10;
--z-sticky:        100;
--z-overlay:       200;
--z-modal:         300;
--z-toast:         400;
```

---

## CSS Output Format

```css
/* ============================================
   [Project Name] Design System
   Generated by UI/UX Agency Skill System
   ============================================ */

:root {

  /* ─── Colors: Primary ─── */
  --color-primary-50: [value];
  ...

  /* ─── Colors: Neutral ─── */
  ...

  /* ─── Colors: Semantic ─── */
  ...

  /* ─── Colors: State ─── */
  --color-error:   [value];
  --color-success: [value];
  --color-warning: [value];

  /* ─── Typography: Fonts ─── */
  ...

  /* ─── Typography: Size ─── */
  ...

  /* ─── Typography: Weight ─── */
  ...

  /* ─── Typography: Line Height ─── */
  ...

  /* ─── Typography: Letter Spacing ─── */
  ...

  /* ─── Spacing ─── */
  ...

  /* ─── Radius ─── */
  ...

  /* ─── Shadows ─── */
  ...

  /* ─── Motion ─── */
  ...

  /* ─── Breakpoints ─── */
  ...

  /* ─── Layout ─── */
  ...
}
```

---

## JSON Token Format (W3C Design Token Spec)

```json
{
  "$schema": "https://tr.designtokens.org/format/",
  "metadata": {
    "project": "[Project Name]",
    "generated_by": "UI/UX Agency Skill System",
    "version": "1.0"
  },
  "color": {
    "primary": {
      "50":  { "$value": "[hex]", "$type": "color" },
      "100": { "$value": "[hex]", "$type": "color" },
      "500": { "$value": "[hex]", "$type": "color", "$description": "Main brand color" },
      "900": { "$value": "[hex]", "$type": "color" }
    },
    "neutral": {
      "0":   { "$value": "#ffffff", "$type": "color" },
      "50":  { "$value": "[hex]",   "$type": "color" },
      "900": { "$value": "[hex]",   "$type": "color" }
    },
    "semantic": {
      "bg-primary":    { "$value": "{color.neutral.0}",   "$type": "color" },
      "text-primary":  { "$value": "{color.neutral.900}", "$type": "color" },
      "accent":        { "$value": "{color.primary.500}", "$type": "color" }
    }
  },
  "typography": {
    "font-family": {
      "heading": { "$value": "[font stack]", "$type": "fontFamily" },
      "body":    { "$value": "[font stack]", "$type": "fontFamily" }
    },
    "font-size": {
      "base": { "$value": "1rem",   "$type": "dimension" },
      "xl":   { "$value": "1.5rem", "$type": "dimension" }
    }
  },
  "spacing": {
    "4":  { "$value": "1rem",  "$type": "dimension" },
    "8":  { "$value": "2rem",  "$type": "dimension" },
    "16": { "$value": "4rem",  "$type": "dimension" }
  },
  "radius": {
    "card":   { "$value": "1rem",  "$type": "dimension" },
    "button": { "$value": "0.5rem", "$type": "dimension" }
  }
}
```

---

## Tailwind Config Extension Block

Also generate a `tailwind.config.js` extension block:

```js
// tailwind.config.js extend block — paste into theme.extend
module.exports = {
  theme: {
    extend: {
      colors: {
        primary: {
          50:  '[hex]',
          100: '[hex]',
          500: '[hex]',
          900: '[hex]',
        },
        neutral: {
          0:   '#ffffff',
          50:  '[hex]',
          900: '[hex]',
        },
      },
      fontFamily: {
        heading: ['[Font Name]', 'sans-serif'],
        body:    ['[Font Name]', 'sans-serif'],
      },
      fontSize: {
        // uses CSS custom property references
      },
      borderRadius: {
        card:   '1rem',
        button: '0.5rem',
      },
      boxShadow: {
        card:  '...',
        modal: '...',
      },
      transitionDuration: {
        fast:   '150ms',
        base:   '250ms',
        slow:   '400ms',
      },
    },
  },
};
```

---

## Validation

Before writing output, verify:

- [ ] Every color in Design DNA has a CSS token
- [ ] Every font in Design DNA has a font-family token
- [ ] Every spacing value mentioned in Developer Handoff has a token
- [ ] Every radius used in component inventory has a semantic token
- [ ] Semantic tokens reference palette tokens (not raw values)
- [ ] JSON token file is valid JSON
- [ ] CSS file has no syntax errors (check for missing semicolons, unclosed values)
- [ ] Token naming follows `--[category]-[variant]` convention throughout

---

## Project Memory Behavior

**Skill Number:** 08.5
**Reads from:** `.agency/DESIGN_DNA.md`, `.agency/DEVELOPER_HANDOFF.md`
**Writes to:** `.agency/DESIGN_SYSTEM.css`, `.agency/DESIGN_SYSTEM_TOKENS.json`

Before running:

1. Check `.agency/` exists.
2. Read `.agency/CURRENT_CONTEXT.md`.
3. Read `.agency/CONTEXT_INDEX.json`.
4. Read `DESIGN_DNA.md` and `DEVELOPER_HANDOFF.md`.
5. Do not read files not listed above.

---

## Session Resume Behavior

1. Do not ask user to repeat context.
2. Read `.agency/CURRENT_CONTEXT.md` and `CONTEXT_INDEX.json`.
3. Read `DESIGN_DNA.md` and `DEVELOPER_HANDOFF.md`.
4. If `DESIGN_SYSTEM.css` partially exists, continue from where it stopped.
5. Do not regenerate tokens already written.

---

## Post-Task Update Behavior

After completing this skill:

1. Save CSS to `.agency/DESIGN_SYSTEM.css`.
2. Save tokens JSON to `.agency/DESIGN_SYSTEM_TOKENS.json`.
3. Update `.agency/CURRENT_CONTEXT.md`:
   - Mark design-system-export as complete
4. Update `.agency/PROJECT_STATE.json`:
   - Set `design_system_export.status` to `complete`
5. Update `.agency/CONTEXT_INDEX.json`:
   - Set `current_skill` to `developer-handoff` or mark as ready for development
6. Append to `.agency/CHANGELOG.md`.
7. Update `.agency/TODO.md`.
8. Do not delete previous content.

---

## Example Trigger Phrases

- "Export the design system."
- "Generate CSS tokens."
- "Create design tokens from Design DNA."
- "I need the Tailwind config for this project."
- "Generate the token JSON for Figma."
- "Create the CSS variables file."
- "Export tokens for the developer."
