# EaseMotion Infinite Carousel (Glassmorphism)

A pure CSS, JavaScript-free auto-scrolling infinite carousel wrapped in a premium frosted-glass (Glassmorphism) aesthetic. 

## Features
- **Zero JS Dependencies:** Achieves a seamless, infinite loop using meticulously calculated CSS `@keyframes` and `transform: translateX`.
- **Interactive:** Built-in `animation-play-state: paused` logic halts the carousel when a user hovers over a card with their mouse or tabs into a link with their keyboard.
- **Glassmorphism Aesthetic:** Translucent backgrounds, `backdrop-filter: blur`, dynamic background shapes, and floating gradient masks create a deep, modern 3D depth effect.
- **Accessible & Performant:** Hardware-accelerated transforms ensure a 60fps scroll.
- **Reduced Motion Fallback:** For users utilizing OS-level `prefers-reduced-motion`, the auto-scroll animation is killed entirely. The wrapper elegantly degrades into a native, swipeable, horizontal `scroll-snap` container.

## Usage

To achieve the "infinite loop" effect purely in CSS, you must **duplicate your set of cards once**.

1. Place your cards within `.em-carousel-track`.
2. Duplicate the exact set of cards immediately after the first set.
3. Apply `aria-hidden="true"` and `tabindex="-1"` to all links on the **duplicated set**. This ensures screen readers and keyboard navigators do not interact with the duplicated "phantom" elements.

```html
<section class="em-carousel-wrapper">
  <!-- Optional Gradient Masks -->
  <div class="em-carousel-mask em-mask-left"></div>
  <div class="em-carousel-mask em-mask-right"></div>

  <div class="em-carousel-track">
    <!-- 1. Original Set -->
    <div class="em-glass-card"> Card 1 </div>
    <div class="em-glass-card"> Card 2 </div>

    <!-- 2. Duplicated Set (Hidden from Screen Readers) -->
    <div class="em-glass-card" aria-hidden="true"> Card 1 </div>
    <div class="em-glass-card" aria-hidden="true"> Card 2 </div>
  </div>
</section>
