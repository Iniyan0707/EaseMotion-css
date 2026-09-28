# EaseMotion Animated Vertical Timeline (Claymorphism)

A pure CSS, JavaScript-free interactive vertical timeline featuring the signature soft, fluffy, 3D aesthetics of **Claymorphism**.

## Features
- **Zero JS Dependencies:** Interactions (expanding nodes to view details) are handled entirely through structural HTML (`<input type="checkbox">` and `<label>` pairs) mapped via CSS grid animations.
- **Claymorphism Aesthetic:** Utilizes heavy border-radiuses (`28px`), pastel tones, and complex `inset` drop shadows (mimicking light and dark depth) to create physical, puffy-looking UI elements.
- **Staggered Animations:** Timeline nodes automatically float into place using CSS `@keyframes` and staggered `animation-delay` directives mapping to a bouncy `cubic-bezier` curve.
- **Responsive Shape-Shifting:** Employs an alternating left/right layout intersecting a central 3D pipe on desktop devices. On mobile `<768px`, the pipeline automatically collapses to the left rail to maintain readability.
- **Modern Grid Expansions:** Expands/collapses heights perfectly without hacky `max-height` values by transitioning `grid-template-rows: 0fr -> 1fr`.
- **Accessible:** Features interactive `role="button"`, custom `focus-visible` outlines, and completely halts animations natively if `prefers-reduced-motion: reduce` is enabled by the OS.

## Usage

Construct your timeline by repeating `.em-timeline-item` nodes inside the `.em-timeline` wrapper.

1. Ensure the `<input class="em-timeline-toggle">` uses a unique `id`.
2. Connect that unique `id` to the `<label class="em-timeline-label">` via the `for` attribute.
3. Content placed within `.em-timeline-details` will natively expand smoothly when clicked.

```html
<div class="em-timeline">
  <div class="em-timeline-item">
    
    <!-- 3D Node on the timeline pipe -->
    <div class="em-timeline-node"></div>
    
    <div class="em-timeline-content em-clay-card">
      <!-- 1. State Manager -->
      <input type="checkbox" id="unique-step-1" class="em-timeline-toggle" aria-hidden="true" />
      
      <!-- 2. Trigger -->
      <label for="unique-step-1" class="em-timeline-label" tabindex="0" role="button">
        <h3>Step Title</h3>
        <div class="em-clay-btn"><span class="em-chevron"></span></div>
      </label>
      
      <!-- 3. Expanding Content -->
      <div class="em-timeline-details-container">
        <div class="em-timeline-details">
           <p>Your description goes here.</p>
        </div>
      </div>
      
    </div>
  </div>
</div>
