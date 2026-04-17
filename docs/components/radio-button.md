# Radio Button

Radio buttons let users select exactly one option from a set. Unlike checkboxes, only one radio button in a group can be selected at a time.

---

## Variants

### States
| State | Description |
|---|---|
| Default | Unselected, available |
| Selected (Clicked) | Currently selected option |
| Disabled | Cannot be interacted with |
| Selected Disabled | Selected but cannot be changed |

---

## Usage

**Do**
- Use radio buttons when the user must pick exactly one option from 2–4 choices
- Show all options visible at once (no hidden options)
- Group related radio buttons under a clear heading

**Don't**
- Don't use radio buttons for more than 5 options — use a Dropdown instead
- Don't pre-select an option unless there is a clear and safe default
- Don't use a single radio button — always provide at least two

---

## Code

```html
<!-- Radio group -->
<fieldset>
  <legend>Deal Type</legend>

  <label class="radio-wrapper">
    <input type="radio" name="deal-type" value="cash">
    <div class="radio"></div>
    <span class="radio-label">Cash Buyout</span>
  </label>

  <label class="radio-wrapper">
    <input type="radio" name="deal-type" value="contingency">
    <div class="radio radio--selected"></div>
    <span class="radio-label">Contingency</span>
  </label>

  <label class="radio-wrapper">
    <input type="radio" name="deal-type" value="undecided" disabled>
    <div class="radio radio--disabled"></div>
    <span class="radio-label">Undecided</span>
  </label>
</fieldset>
```

### CSS classes reference
```
.radio-wrapper     Clickable row wrapper
.radio             The visual circle
.radio--selected   Selected state (filled centre dot)
.radio--disabled   Disabled state
.radio-label       Label text
```
