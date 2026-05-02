# Alert (Feedback)

Full-width notification banners for system feedback. Dismissible via the close button.

## Types
- `alert--information` — Blue, for tips and guidance
- `alert--success` — Green, for completed actions
- `alert--error` — Red, for failures and errors
- `alert--warning` — Orange, for cautionary messages

## Usage
```html
<div class="alert alert--success">
  <svg class="alert__icon">...</svg>
  <div class="alert__body">
    <p class="alert__title">Success</p>
    <p class="alert__message">Your changes have been saved.</p>
  </div>
  <button class="alert__close" onclick="this.closest('.alert').classList.add('alert--dismissed')">
    ×
  </button>
</div>
```
