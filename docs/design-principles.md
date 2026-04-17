# Design Principles — AssetTrace

## 1. Clarity over decoration
Every visual element should serve a purpose. When in doubt, remove it.

## 2. Consistency builds trust
Use the same component for the same job everywhere. Do not introduce one-off variations.

## 3. Token-first
Never hardcode a color, font size, or spacing value. Always reference a token. This ensures the whole system updates together.

## 4. States matter
Every interactive component must have a clear visual state for: Default, Hover, Active/Focused, Disabled, Error, and Success.

## 5. Accessible by default
All components are designed to meet WCAG 2.1 AA contrast requirements.

---

*These principles apply to both design decisions in Figma and code decisions in this repository.*