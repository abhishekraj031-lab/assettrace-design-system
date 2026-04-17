# Button

Buttons trigger actions. They are the primary way users interact with the product.

---

## Variants

### Types
| Type | When to use |
|---|---|
| **Filled** | Primary action on a page — the most important thing a user can do |
| **Outline** | Secondary action that sits alongside a Filled button |
| **Text** | Tertiary or low-emphasis action, or inline links within content |

### Sizes
| Size | Height | When to use |
|---|---|---|
| Large | 44px | Default size for most actions |
| Medium | 40px | Compact layouts, tables, sidebars |
| Small | 36px | Dense UIs, inline actions |

### States
| State | Description |
|---|---|
| Default | Normal resting state |
| Hover | User's cursor is over the button |
| Active / Clicked | Button is being pressed |
| Disabled | Action is not available |
| Success | Confirms a successful outcome (e.g. "Saved") |
| Warning | Warns before a potentially risky action |
| Information | Neutral informational action |
| Destructive | Irreversible or dangerous action (e.g. "Delete") |

---

## Usage

**Do**
- Use one Filled button per section — it should be the primary action
- Always label buttons with a verb ("Save", "Add Asset", "Delete")
- Use Destructive state for any action that cannot be undone

**Don't**
- Don't use more than two buttons side by side (primary + secondary max)
- Don't use Filled + Filled together — one should always be Outline or Text
- Don't disable buttons without explaining why elsewhere on the page

---

## Code

### HTML structure
```html
<!-- Filled — Large (default) -->
<button class="btn btn--filled btn--lg">Save Changes</button>

<!-- Filled — Medium -->
<button class="btn btn--filled btn--md">Save Changes</button>

<!-- Filled — Small -->
<button class="btn btn--filled btn--sm">Save Changes</button>

<!-- Outline -->
<button class="btn btn--outline btn--lg">Cancel</button>

<!-- Text -->
<button class="btn btn--text btn--lg">Learn More</button>

<!-- With icon (left) -->
<button class="btn btn--filled btn--lg">
  <span class="btn__icon"><!-- SVG icon here --></span>
  Add Asset
</button>

<!-- With icon (both sides) -->
<button class="btn btn--filled btn--lg">
  <span class="btn__icon"><!-- left icon --></span>
  Add Asset
  <span class="btn__icon"><!-- right icon (chevron etc) --></span>
</button>

<!-- Disabled -->
<button class="btn btn--filled btn--lg" disabled>Save Changes</button>

<!-- Semantic states -->
<button class="btn btn--filled btn--lg btn--success">Saved!</button>
<button class="btn btn--filled btn--lg btn--destructive">Delete Asset</button>
<button class="btn btn--filled btn--lg btn--warning">Archive</button>
<button class="btn btn--filled btn--lg btn--information">View Details</button>
```

### CSS classes reference
```
.btn                  Base button — required on all buttons
.btn--filled          Filled type
.btn--outline         Outline type
.btn--text            Text type
.btn--lg              Large size (44px)
.btn--md              Medium size (40px)
.btn--sm              Small size (36px)
.btn--success         Success semantic state
.btn--warning         Warning semantic state
.btn--information     Information semantic state
.btn--destructive     Destructive semantic state
```

---

## Accessibility
- Always use a `<button>` element (not `<div>` or `<span>`)
- Disabled buttons should have `disabled` attribute (not just a CSS class)
- Icon-only buttons must have `aria-label="action name"`
- Minimum touch target: 44×44px (Large size meets this by default)
