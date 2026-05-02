# Tooltip

Provides brief contextual help on hover. Supports 8 arrow placements.

## Arrow Positions
```
tooltip--bottom-left    tooltip--bottom-centre    tooltip--bottom-right
tooltip--top-left       tooltip--top-centre       tooltip--top-right
tooltip--left-centre    tooltip--right-centre
```

## Usage
Wrap the trigger and tooltip together in `.tooltip-wrapper`:

```html
<div class="tooltip-wrapper">
  <button>Hover me</button>
  <div class="tooltip tooltip--bottom-centre">
    Helpful context text
  </div>
</div>
```

Tooltip appears on hover automatically via CSS.
