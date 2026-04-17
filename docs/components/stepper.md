# Stepper

The Stepper shows progress through a multi-step process. It gives users a clear sense of where they are and how many steps remain.

---

## Variants

### Step States
| State | Description |
|---|---|
| Completed | Step is done — filled circle with a checkmark |
| Active | Current step — highlighted circle with step number |
| Pending | Future step — grey empty circle with step number |

---

## Usage

**Do**
- Use the Stepper for processes with 2–6 clear, sequential steps
- Label each step concisely (1–2 words)
- Always show the full stepper so users know how many steps remain

**Don't**
- Don't use a Stepper for non-linear flows where steps can be skipped freely
- Don't exceed 6 steps — break the process into sections instead

---

## Code

```html
<div class="stepper">

  <!-- Completed step -->
  <div class="stepper__step stepper__step--completed">
    <div class="stepper__circle">✓</div>
    <span class="stepper__label">Details</span>
  </div>

  <!-- Active step -->
  <div class="stepper__step stepper__step--active">
    <div class="stepper__circle">2</div>
    <span class="stepper__label">Review</span>
  </div>

  <!-- Pending step -->
  <div class="stepper__step">
    <div class="stepper__circle">3</div>
    <span class="stepper__label">Confirm</span>
  </div>

</div>
```

### CSS classes reference
```
.stepper                        Flex container for the full stepper row
.stepper__step                  Individual step (pending by default)
.stepper__step--active          Current active step
.stepper__step--completed       Completed step
.stepper__circle                The numbered/icon circle
.stepper__label                 Step label text below the circle
```
