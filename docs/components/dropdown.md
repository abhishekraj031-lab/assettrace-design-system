# Dropdown

Dropdowns let users select one option from a list. They are used when there are too many options to show as radio buttons.

---

## Variants

### States
| State | Description |
|---|---|
| Default | Closed, no selection made |
| Hover | Cursor over the dropdown |
| Selected | A value has been chosen |
| Disabled | Cannot be interacted with |
| Disabled Selected | Has a value but cannot be changed |

---

## Usage

**Do**
- Use dropdowns when there are 5 or more options
- Always show a placeholder like "Select option" in the default state
- Sort options logically (alphabetically or by frequency of use)

**Don't**
- Don't use a dropdown for fewer than 4 options — use Radio Buttons instead
- Don't use dropdowns for binary choices — use a Toggle or Checkbox instead

---

## Code

```html
<!-- Default -->
<div class="dropdown-group">
  <label class="dropdown-group__label">Category</label>
  <div class="dropdown">
    <span class="dropdown__text">Select option</span>
    <span class="dropdown__arrow">▾</span>
  </div>
</div>

<!-- Selected -->
<div class="dropdown-group">
  <label class="dropdown-group__label">Category</label>
  <div class="dropdown dropdown--selected">
    <span class="dropdown__text dropdown__text--selected">Cash Buyout</span>
    <span class="dropdown__arrow">▾</span>
  </div>
</div>

<!-- Disabled -->
<div class="dropdown-group">
  <label class="dropdown-group__label">Category</label>
  <div class="dropdown dropdown--disable">
    <span class="dropdown__text">Select option</span>
    <span class="dropdown__arrow">▾</span>
  </div>
</div>
```

### CSS classes reference
```
.dropdown-group              Wrapper (label + field)
.dropdown-group__label       Label above the dropdown
.dropdown                    The dropdown trigger button
.dropdown--selected          Selected state
.dropdown--disable           Disabled state
.dropdown__text              Placeholder or selected text
.dropdown__text--selected    Applied when a value is selected (darker colour)
.dropdown__arrow             The chevron icon
```
