# Glowing Cyberpunk Flyout Popover

A lightweight, zero-JavaScript popover component featuring glowing cyberpunk aesthetics, modern clip-path geometry, and smooth state transition animations using standard HTML5 Popover attributes and EaseMotion design tokens.

## Features

- **Zero JS Dependencies**: Built entirely with native HTML popover attributes (`popover`, `popovertarget`, `popovertargetaction`).
- **EaseMotion Tokens**: Leverages cubic-bezier timing functions and design tokens for smooth state transitions.
- **Responsive Design**: Automatically switches from relative flyout mode on desktop/tablet to bottom sheet display on small screen viewports.
- **Accessibility**: Includes focus states, proper ARIA attributes, and explicit `prefers-reduced-motion` CSS overrides.

## Usage

1. Link `style.css` in your HTML document.
2. Bind the trigger element to the popover element using the `popovertarget` ID reference:

```html
<button popovertarget="my-popover">Open</button>

<div id="my-popover" popover class="cyber-popover">
  <!-- Content -->
</div>
