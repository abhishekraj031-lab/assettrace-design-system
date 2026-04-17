# Design Tokens

Design tokens are the foundation of the AssetTrace design system. Every color, font size, spacing value, and border radius is defined as a token. Components use tokens — never raw values.

---

## Token Files

| File | Description | Variables |
|---|---|---|
| `tokens/colors.css` | Full color palette | 102 |
| `tokens/semantic-colors.css` | Semantic color tokens | 57 |
| `tokens/spacing.css` | Spacing + border radius | 21 |
| `tokens/typography.css` | Font sizes, weights, line heights | 15 styles |
| `tokens/tokens.json` | Master file — all tokens in JSON | All |

---

## How to use tokens

Import the token files in your HTML:
```html
<link rel="stylesheet" href="tokens/colors.css">
<link rel="stylesheet" href="tokens/semantic-colors.css">
<link rel="stylesheet" href="tokens/spacing.css">
<link rel="stylesheet" href="tokens/typography.css">
```

Then use the CSS variables anywhere:
```css
.my-element {
  background-color: var(--color-brand-500);
  color: var(--typography-white);
  padding: var(--spacing-m) var(--spacing-xxl);
  border-radius: var(--radius-s);
  font-size: var(--font-label-l1-semibold-size);
  font-weight: var(--font-label-l1-semibold-weight);
}
```

**Rule:** Always use a semantic token in components. Only use palette tokens when no semantic token exists.

---

## Color Palette

10 color families × 10 shades (50–900) + Grey (0–1000)

| Family | Usage |
|---|---|
| `--color-brand-*` | Primary product color — brand blue |
| `--color-blue-*` | Informational states, links |
| `--color-green-*` | Success, positive outcomes |
| `--color-orange-*` | Warnings, needs attention |
| `--color-red-*` | Errors, destructive actions |
| `--color-yellow-*` | Caution states |
| `--color-purple-*` | Accent |
| `--color-magenta-*` | Accent |
| `--color-teal-*` | Accent |
| `--color-grey-*` | Neutral UI — backgrounds, borders, text |

---

## Semantic Colors

Use these tokens in all components. They map to a palette color and carry meaning.

### Surface
```
--surface-default        White — main page/card background
--surface-light          Grey/100 — subtle background
--surface-brand          Brand/500 — primary brand surface
--surface-disable        Grey/50 — disabled element background
--surface-information    Blue/50 — info context background
--surface-success        Green/50 — success context background
--surface-warning        Orange/50 — warning context background
--surface-error          Red/50 — error context background
--surface-caution        Yellow/50 — caution context background
```

### Typography
```
--typography-default     Grey/700 — primary body text
--typography-light       Grey/500 — secondary / muted text
--typography-placeholder Grey/400 — input placeholder text
--typography-disable     Grey/400 — disabled text
--typography-white       White — text on dark/brand backgrounds
--typography-information Blue/600
--typography-success     Green/600
--typography-warning     Orange/400
--typography-error       Red/500
--typography-caution     Yellow/500
```

### Border
```
--border-default         Grey/200 — default element border
--border-button-default  Brand/500
--border-button-hover    Brand/600
--border-button-clicked  Brand/700
--border-button-disable  Grey/300
--border-information     Blue/500
--border-success         Green/500
--border-warning         Orange/500
--border-error           Red/500
```

### Button Backgrounds
```
--button-default         Brand/500 (#2778e2)
--button-hover           Brand/600 (#1d62c0)
--button-clicked         Blue/700  (#0277c5)
--button-disable         Grey/100  (#f1f5f9)
--button-success         Green/500 (#10b981)
--button-warning         Orange/500 (#f97316)
--button-information     Blue/500  (#1ca3fd)
--button-destructive     Red/500   (#ef4444)
```

---

## Spacing

12 spacing tokens from 0 to 40px.

| Token | Value | Usage example |
|---|---|---|
| `--spacing-none` | 0px | No spacing |
| `--spacing-xxs` | 2px | Micro gaps |
| `--spacing-xs` | 4px | Tight gaps (icon to label) |
| `--spacing-s` | 6px | Small padding |
| `--spacing-m` | 8px | Default gap between elements |
| `--spacing-l` | 10px | Comfortable gap |
| `--spacing-xl` | 12px | Medium padding |
| `--spacing-xxl` | 16px | Standard section padding |
| `--spacing-3xl` | 20px | Large gap |
| `--spacing-4xl` | 24px | Component padding |
| `--spacing-5xl` | 32px | Section spacing |
| `--spacing-6xl` | 40px | Large section spacing |

---

## Border Radius

| Token | Value | Usage |
|---|---|---|
| `--radius-none` | 0px | Square corners |
| `--radius-xxs` | 2px | Subtle rounding |
| `--radius-xs` | 4px | Chip/tag radius |
| `--radius-s` | 6px | **Default** — buttons, inputs, dropdowns |
| `--radius-m` | 8px | Cards |
| `--radius-l` | 10px | Modals |
| `--radius-xl` | 12px | Larger cards |
| `--radius-xxl` | 16px | Panels |
| `--radius-xxxl` | 20px | Large rounded containers |

---

## Typography

Font: **Poppins** (loaded from Google Fonts)

| Style | Size | Weight | Line Height | Usage |
|---|---|---|---|---|
| Heading/H1 | 48px | 700 | 110% | Page titles |
| Heading/H2 | 40px | 700 | 110% | Section titles |
| Heading/H3 | 36px | 700 | 110% | Sub-section titles |
| Heading/H4 | 32px | 700 | 110% | Card headings |
| Heading/H5 | 28px | 700 | 110% | Smaller headings |
| Heading/H6 | 24px | 700 | 110% | Smallest heading |
| Body/B1 | 20px | 600 | 125% | Large body text |
| Body/B2 | 16px | 600 | 125% | Standard body text |
| Label/L1/Regular | 14px | 400 | 130% | Form labels, descriptions |
| Label/L1/Medium | 14px | 500 | 130% | Emphasized labels |
| Label/L1/SemiBold | 14px | 600 | 130% | Button text, strong labels |
| Label/L2/Regular | 12px | 400 | 140% | Helper text, captions |
| Label/L2/Medium | 12px | 500 | 140% | Small emphasized text |
| Label/L2/SemiBold | 12px | 600 | 140% | Small strong labels |
| Label/L3/Regular | 11px | 400 | 150% | Micro labels, tags |

### Using typography utility classes
```html
<h1 class="text-heading-h1">Page Title</h1>
<p class="text-body-b2">Body paragraph text</p>
<span class="text-label-l1-semibold">Button label</span>
<small class="text-label-l2-regular">Helper text</small>
```
