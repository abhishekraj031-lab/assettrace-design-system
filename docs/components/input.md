# Input

Text inputs let users enter and edit information. Every input has a label, a field, and optional helper text.

---

## Variants

### Types
| Type | Description |
|---|---|
| Default | Plain text input |
| Text First | Prefix text before the input (e.g. "+1" for phone) |
| Icon First | Icon on the left inside the field |
| Text Last | Suffix text after the input (e.g. unit labels) |
| Icon Last | Icon on the right inside the field |

### States
| State | Description |
|---|---|
| Default | Resting, unfocused |
| Hover | Cursor over the field |
| Active | Field is focused and ready for input |
| Filled | Field has a value entered |
| Disabled | Input cannot be interacted with |
| Filled Disabled | Has a value but cannot be edited |
| Error | Validation failed — red border + red helper text |

---

## Usage

**Do**
- Always include a label above every input
- Use helper text to explain format requirements (e.g. "Must be a valid email")
- Show error state with a specific message explaining what went wrong

**Don't**
- Don't use placeholder text as a label substitute — labels must always be visible
- Don't show error state before the user has interacted with the field
- Don't stack more than one prefix/suffix on the same input

---

## Code

```html
<!-- Default input -->
<div class="input-group">
  <label class="input-group__label">Email</label>
  <div class="input-field">
    <input type="text" placeholder="Enter Email">
  </div>
  <span class="input-group__helper">Help text will be shown here</span>
</div>

<!-- With prefix text -->
<div class="input-group">
  <label class="input-group__label">Phone</label>
  <div class="input-field">
    <span class="input-field__prefix">+1</span>
    <input type="tel" placeholder="Enter number">
  </div>
</div>

<!-- With suffix icon -->
<div class="input-group">
  <label class="input-group__label">Email</label>
  <div class="input-field">
    <input type="email" placeholder="Enter Email">
    <span class="input-field__icon"><!-- SVG icon --></span>
  </div>
</div>

<!-- Error state -->
<div class="input-group input-group--error">
  <label class="input-group__label">Email</label>
  <div class="input-field">
    <input type="email" placeholder="Enter Email">
  </div>
  <span class="input-group__helper">Please enter a valid email address</span>
</div>

<!-- Disabled state -->
<div class="input-group input-group--disable">
  <label class="input-group__label">Email</label>
  <div class="input-field">
    <input type="text" placeholder="Enter Email" disabled>
  </div>
  <span class="input-group__helper">Help text here</span>
</div>
```

### CSS classes reference
```
.input-group              Wrapper for the full input (label + field + helper)
.input-group__label       Label text above the field
.input-group__helper      Helper/error text below the field
.input-group--error       Error state — red border and helper text
.input-group--disable     Disabled state
.input-field              The input box itself
.input-field__prefix      Text prefix inside the field (left)
.input-field__suffix      Text suffix inside the field (right)
.input-field__icon        Icon inside the field
```

---

## Accessibility
- Label must always be visible and associated with the input via `for`/`id` or wrapping
- Error messages should use `role="alert"` or `aria-describedby` pointing to the helper text
- Disabled inputs should use the `disabled` HTML attribute
