# Guardio Design Kit — Instructions for Claude

You are building a Guardio web page. Before you write a single line of HTML or CSS, read the attached `Guardio-Website-design-kit.html` file in full. Everything you need is already defined there — colors, typography, buttons, cards, section layouts, spacing, and components. Your job is to assemble pages from those existing patterns, not to invent new ones.

---

## Rules

**1. Use only what's in the kit.**
Do not introduce new fonts, colors, border radii, shadow styles, or layout patterns. If a design decision isn't in the kit, pick the closest existing one and use that.

**2. Always link `partners.css`.**
Every new page must start with:
```html
<link rel="stylesheet" href="partners.css" />
```
Do not write inline styles or new CSS classes unless absolutely unavoidable. If you must add something new, add it as a CSS variable override at the top of a `<style>` block, not inline.

**3. Use the exact design tokens.**
| Token | Value | Use for |
|---|---|---|
| `--color-navy` | `#1c2135` | Headlines, dark sections, dark buttons |
| `--color-blue` | `#2e69ff` | Primary CTAs, links, accents |
| `--color-green` | `#14ae5c` | Success, secure, checkmarks |
| `--color-red` | `#fb462d` | Alerts, warnings, threats |
| `--color-badge-blue` | `#d4dbf6` | Badges, tags |
| `--color-bg-light` | `#f6f6f6` | Alternate section backgrounds |
| `--color-border` | `#d8e2ea` | Card borders, dividers |
| `--color-text-muted` | `#6d6d6d` | Secondary text, captions |
| Font | `Inter, sans-serif` | Everything |

**4. Use the exact type scale.**
| Element | Size | Weight |
|---|---|---|
| Hero headline (H1) | 60px | 500 |
| Section title (H2) | 40px | 500 |
| Card title (H3) | 24px | 500 |
| Lead paragraph | 20px | 400 |
| Body / nav | 16px | 400–500 |
| Caption / small | 14px | 400 |

**5. Use the correct button styles — no variations.**
- **Primary (blue pill):** `class="btn btn--primary-lg"` or `class="btn btn--primary"`
- **Dark pill:** `class="btn btn--dark"`
- **Ghost (outline on dark bg):** `class="btn btn--outline-white"`
- **Text link with arrow:** `class="btn btn--ghost"`

**6. Section backgrounds follow this pattern only:**
- White: `class="section section--white"`
- Light gray: `class="section section--light"`
- Dark navy: `class="section section--dark"`

**7. Always include the standard nav and footer.**
Copy the nav and footer blocks from any of the existing partner pages (`index.html`, `affiliates.html`, `it-repair.html`). Update the active nav link for the current page by adding `g-nav__link--active` to the right item.

**8. Cards use these shadow and radius values only.**
```css
border-radius: 10px; /* --radius-md */
box-shadow: rgba(174, 174, 174, 0.2) 0px 5px 20px 0px; /* --shadow-card */
```

---

## How to build a new page

Tell Claude what the page is about and what sections it needs. For example:

> "Build a new Guardio partner page for resellers. It needs a hero section, a 3-column value prop block, a how-it-works stepper, and a signup form. Use the design kit."

Claude will assemble it from the components in the kit. You do not need to describe colors, fonts, or spacing — those are already locked in.

---

## What to hand Claude

When starting a new page, attach these two files to your conversation:
1. `Guardio-Website-design-kit.html` — the visual reference
2. `partners.css` — the shared stylesheet

Then describe the page in plain English. Claude handles the rest.

---

## What not to ask Claude to do

- ❌ "Make it look more modern" — the style is already defined
- ❌ "Use a different blue" — use `--color-blue` (#2e69ff) only
- ❌ "Add a gradient background" — not in the kit
- ❌ "Use Tailwind / Bootstrap" — use `partners.css` only

If you genuinely need a new component that isn't in the kit, flag it to the team first so it can be added to the kit properly and stay consistent across all pages.

---

*Guardio Design Kit · Last updated April 2026*
