# Getting Started with the AssetTrace Design System

## For Developers

### Using Tokens

Copy the CSS files from the `tokens/` folder into your project and import them:

```html
<link rel="stylesheet" href="tokens/colors.css">
<link rel="stylesheet" href="tokens/semantic-colors.css">
<link rel="stylesheet" href="tokens/typography.css">
```

Then use the CSS variables anywhere in your styles:

```css
.my-button {
  background-color: var(--brand-500);
  color: var(--grey-0);
  font-size: var(--font-size-label-l1);
}
```

### Using Components

Each component in the `components/` folder contains:
- An `.html` file showing example markup
- A `.css` file with all styles

Copy the CSS into your project and use the HTML as a reference.

---

## For Designers

The Figma file is the source of truth. All code in this repository is generated from Figma.

**Figma file:** Design-System_V.2.0

When you update a component in Figma, notify the team and the code will be synced automatically.

---

## Fonts

This design system uses **Poppins**. Make sure it is loaded in your project:

```html
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">
```