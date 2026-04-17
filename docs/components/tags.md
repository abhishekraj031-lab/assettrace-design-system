# Tags, Chips & Badge

These components display short labels, status indicators, and categorisation pills. There are three distinct variants: Status Chip, Chip, and Badge.

---

## Variants

### Status Chip
Small pill-shaped labels used to show the current status of an item (e.g. "In Review", "Offered", "Declined"). Used in tables, cards, and lists.

| Colour | Semantic meaning |
|---|---|
| Blue | Informational / In Progress |
| Green | Success / Positive |
| Orange | Warning / Needs attention |
| Red | Error / Declined |
| Yellow | Caution |
| Grey | Neutral / Closed |
| Brand | Active / Primary |

Each colour has a **Light** (outlined) and **Dark** (filled) variant.

### Chip
Medium-sized tags used for categorisation or filtering. Slightly larger than a Status Chip, with a rectangular border radius.

### Badge
The largest tag variant. Used for prominent category labels, deal types, or classification within cards and detail views.

---

## Usage

**Do**
- Use Status Chip for live status information that changes (pipeline stage, review state)
- Use Chip for static category labels (deal type, asset class)
- Use Badge for the most prominent classification on a card or header

**Don't**
- Don't mix Status Chip and Badge in the same context — pick one level of emphasis
- Don't use more than 2–3 chips on a single row or card
- Don't truncate chip text — keep labels short (1–3 words max)

---

## Code

```html
<!-- Status Chip — Light variants -->
<span class="status-chip status-chip--blue">In Review</span>
<span class="status-chip status-chip--green">Offered</span>
<span class="status-chip status-chip--orange">Agreement</span>
<span class="status-chip status-chip--red">Declined</span>
<span class="status-chip status-chip--grey">Withdraw</span>
<span class="status-chip status-chip--brand">Active</span>

<!-- Status Chip — Dark variants -->
<span class="status-chip status-chip--blue-dark">In Review</span>
<span class="status-chip status-chip--green-dark">Offered Accepted</span>
<span class="status-chip status-chip--grey-dark">Closed</span>

<!-- Chip — Rectangular -->
<span class="chip chip--blue">Cash Buyout</span>
<span class="chip chip--orange">Contingency</span>
<span class="chip chip--grey">Undecided</span>

<!-- Chip — Round -->
<span class="chip chip--round chip--blue">In Review</span>
<span class="chip chip--round chip--green">Offered</span>

<!-- Badge -->
<span class="badge">Cash Buyout</span>
<span class="badge badge--filled-blue">Cash Buyout</span>
<span class="badge badge--filled-orange">Contingency</span>
<span class="badge badge--filled-grey">Undecided</span>
```

### CSS classes reference
```
.status-chip                Base status chip
.status-chip--[colour]      Light colour variant (blue/green/orange/red/yellow/grey/brand)
.status-chip--[colour]-dark Dark filled variant

.chip                       Base chip
.chip--round                Round border radius variant
.chip--[colour]             Chip colour (blue/orange/grey)

.badge                      Base badge (outline style)
.badge--filled-blue         Filled blue badge
.badge--filled-orange       Filled orange badge
.badge--filled-grey         Filled grey badge
```
