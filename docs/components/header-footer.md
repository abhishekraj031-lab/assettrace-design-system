# Header & Footer

Application shell components providing consistent navigation and page framing.

## Header States
- `header` (base) — Default header container (64px tall)
- **Only Logo** — Logo only, no nav
- **With Profile** — Full header: logo, nav, search, avatar
- **Active Profile** — Profile dropdown is open (`.header__profile--active`)

## Search Bar
```html
<div class="search-bar">
  <span class="search-bar__icon"><!-- search SVG --></span>
  <input class="search-bar__input" type="text" placeholder="Search…">
</div>
<!-- Filled state -->
<div class="search-bar search-bar--filled">…</div>
```

## Footer Variants
```html
<footer class="footer">…</footer>                       <!-- Default -->
<footer class="footer footer--with-border">…</footer>   <!-- With top border -->
```
