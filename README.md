# AssetTrace Design System

> The single source of truth for all UI components, design tokens, and guidelines used in the AssetTrace product.

---

## What is this?

This repository contains everything needed to build consistent, on-brand UI for AssetTrace — a SaaS web application. It is generated directly from our Figma design file and kept in sync automatically.

**Design source:** Figma (Design-System_V.2.0)  
**Font:** Poppins  
**Maintained by:** Abhishek

---

## Repository Structure

```
assettrace-design-system/
├── tokens/          ← Color, typography, and spacing variables (CSS + JSON)
├── components/      ← One folder per UI component (HTML + CSS)
├── icons/           ← All icons as SVG files
├── docs/            ← Usage guides and design principles
└── assets/          ← Logos and other brand assets
```

---

## Tokens

Design tokens are the foundation of the system — they define every color, font size, and spacing value. All components use these tokens so that changing a token updates everything that uses it.

| File | What it contains |
|---|---|
| `tokens/colors.css` | All color palette variables (102 colors) |
| `tokens/semantic-colors.css` | Semantic color tokens (78 tokens) |
| `tokens/typography.css` | Font sizes, weights, and line heights |
| `tokens/tokens.json` | Master token file (all tokens in one place) |

---

## Components

| Component | Variants | Status |
|---|---|---|
| Button | 84 | 🔜 Coming soon |
| Input | 35 | 🔜 Coming soon |
| Dropdown | 5 | 🔜 Coming soon |
| Checkbox | 10 | 🔜 Coming soon |
| Radio Button | 4 | 🔜 Coming soon |
| Tags / Chips | 26 | 🔜 Coming soon |
| Header | 3 | 🔜 Coming soon |
| Footer | 2 | 🔜 Coming soon |
| Search Bar | 2 | 🔜 Coming soon |
| Logo | 4 | 🔜 Coming soon |
| Stepper | 3 | 🔜 Coming soon |

---

## How This Repository is Maintained

This design system is synced from Figma using Claude (AI). When a component or token is updated in Figma, only the changed files are updated here — nothing is re-run from scratch.

---

*Last synced: April 17, 2026*
