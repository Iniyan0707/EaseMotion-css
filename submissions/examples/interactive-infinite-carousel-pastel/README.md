# Interactive Infinite Carousel (Pastel Variant)

A zero-JS, pure CSS interactive infinite carousel component styled with a modern pastel color palette and integrated with EaseMotion design tokens.

## Features
- **Zero JavaScript Dependencies**: Entirely driven by CSS animations, hover states, and keyframes.
- **EaseMotion Tokens**: Built using `--easemotion-*` custom properties for unified animation timing and curves.
- **Accessibility Ready**: Fully supports `prefers-reduced-motion: reduce` by degrading gracefully to a standard touch/scroll track with scroll-snap. Includes full focus indicator management and `aria-hidden` attributes on duplicated track nodes.
- **Responsive Layout**: Fluidly scales card sizes across desktop, tablet, and mobile breakpoints.

## Usage
Import `style.css` into your document or bundle process. Ensure the track duplicates the item set to enable seamless 0% -> 100% loop translation.
