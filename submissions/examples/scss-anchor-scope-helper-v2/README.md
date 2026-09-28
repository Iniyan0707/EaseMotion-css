# SCSS CSS Anchor Scope Helper v2

An extension to the EaseMotion SCSS mixin suite that provides simple mixins for working with the native **CSS Anchor Positioning API** while ensuring backward compatibility with fallback absolute positioning.

## Mixins Introduced

### `em-anchor-target($anchor-name)`
Marks an element as an anchor reference node.
```scss
.my-button {
  @include em-anchor-target('--my-anchor');
}
