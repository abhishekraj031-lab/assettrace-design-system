# Checkbox

Checkboxes allow users to select one or more items from a list, or to toggle a single option on or off.

---

## Variants

### States
| State | Description |
|---|---|
| Default | Unchecked, available |
| Selected | Checked |
| Partial | Partially selected (used for parent checkboxes when some children are checked) |
| Selected Disabled | Checked but cannot be changed |
| Disabled | Unchecked and cannot be interacted with |

---

## Usage

**Do**
- Use checkboxes for multi-select (when the user can pick more than one)
- Use the Partial state for "select all" controls when only some children are checked
- Always pair a checkbox with a visible label

**Don't**
- Don't use a checkbox for a single binary action — use a Toggle instead
- Don't require a checkbox to trigger an immediate action

---

## Code

```html
<!-- Default (unchecked) -->
<label class="checkbox-wrapper">
  <input type="checkbox">
  <div class="checkbox"></div>
  <span class="checkbox-label">Accept terms</span>
</label>

<!-- Selected (checked) -->
<label class="checkbox-wrapper">
  <input type="checkbox" checked>
  <div class="checkbox checkbox--selected"></div>
  <span class="checkbox-label">Accept terms</span>
</label>

<!-- Partial -->
<label class="checkbox-wrapper">
  <input type="checkbox">
  <div class="checkbox checkbox--partial"></div>
  <span class="checkbox-label">Select all</span>
</label>

<!-- Disabled -->
<label class="checkbox-wrapper checkbox-wrapper--disabled">
  <input type="checkbox" disabled>
  <div class="checkbox checkbox--disabled"></div>
  <span class="checkbox-label">Unavailable option</span>
</label>
```

### CSS classes reference
```
.checkbox-wrapper            Clickable wrapper row
.checkbox-wrapper--disabled  Disabled wrapper (cursor + label colour)
.checkbox                    The visual checkbox box
.checkbox--selected          Checked state
.checkbox--partial           Indeterminate / partial state
.checkbox--disabled          Disabled state
.checkbox-label              Label text
```

---

## Accessibility
- Use `<input type="checkbox">` — the native element is hidden with CSS but remains accessible to screen readers
- For partial state, also add `indeterminate` property via JavaScript: `input.indeterminate = true`
