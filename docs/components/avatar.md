# Avatar

Represents a user visually — with an image, initials, or an icon. Includes a status indicator.

## Types
- `avatar--image` — Shows a profile photo
- `avatar--text` — Shows 1–2 letter initials
- `avatar--icon` — Shows a fallback person icon

## Sizes
| Class | Size |
|---|---|
| `avatar--xs` | 24 × 24px |
| `avatar--sm` | 32 × 32px |
| `avatar--md` | 40 × 40px |
| `avatar--lg` | 56 × 56px |

## Status
Add a status modifier alongside a `<span class="avatar__status"></span>` inside the avatar:
- `avatar--active` — Green dot
- `avatar--away` — Yellow dot
- `avatar--offline` — Grey dot
- `avatar--busy` — Red dot

## Usage
```html
<div class="avatar avatar--image avatar--md avatar--active">
  <img src="photo.jpg" alt="User name">
  <span class="avatar__status"></span>
</div>

<div class="avatar avatar--text avatar--md">AB</div>
```

## Avatar Group
```html
<div class="avatar-group">
  <div class="avatar avatar--image avatar--md">...</div>
  <div class="avatar avatar--image avatar--md">...</div>
  <div class="avatar avatar--text avatar--md">+4</div>
</div>
```
