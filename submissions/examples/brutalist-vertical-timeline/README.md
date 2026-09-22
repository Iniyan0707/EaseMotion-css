# Brutalist Interactive Vertical Timeline

A high-contrast, zero-JavaScript interactive vertical timeline component featuring bold Neo-Brutalism styling (hard edges, distinct drop shadows, raw typography) paired with smooth state transitions using EaseMotion CSS timing functions and CSS Grid fraction transitions.

## Features

- **Zero JS Dependencies**: Built using standard pure CSS state control via the CSS `:checked` pseudo-class and sibling combinator pattern.
- **Brutalist Design Language**: High-contrast borders, solid offsets, raw color tokens, and hard shadow projections.
- **Smooth Expansion**: Employs CSS Grid (`grid-template-rows: 0fr` to `1fr`) for seamless dynamic content height expansion without requiring hardcoded heights.
- **Responsive Layout**: Adapts gracefully across desktop, tablet, and mobile breakpoints with automatic header restructuring.
- **Accessibility**: Native `:focus-visible` ring indicators and automatic transition suppression via `prefers-reduced-motion: reduce`.

## Usage

1. Include `style.css` inside your HTML header.
2. Structure timeline nodes using checkbox inputs bound to matching card labels:

```html
<section class="timeline-item">
  <input type="checkbox" id="node-1" class="timeline-toggle">
  <div class="timeline-marker">01</div>
  <div class="timeline-card">
    <label for="node-1" class="timeline-card__header">
      <!-- Title & Icon -->
    </label>
    <div class="timeline-card__body">
      <!-- Content -->
    </div>
  </div>
</section>
