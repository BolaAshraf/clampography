# 🙌 Clampography

**Clampography** is a CSS-only alternative to the official
[Tailwind CSS Typography plugin](https://github.com/tailwindlabs/tailwindcss-typography).
Instead of fixed sizes, it uses the CSS
[clamp()](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Values/clamp)
function to create fluid typography that adapts to any screen. With
[94% global browser support](https://caniuse.com/css-math-functions), it works
on nearly all devices.

Built for [Tailwind v4's](https://tailwindcss.com/blog/tailwindcss-v4) CSS-first
architecture. Zero JavaScript configuration required. Best suited for blogs,
documentation, and content-heavy websites.

- **No default styling:** No colors, borders, transforms, or decorations.
- **Structure only:** Manages size, spacing, weight, and font-family.
- **Smart scaling:** Contextual elements use `em` (relative), blocks use
  `clamp()` (fluid).

## Installation

```bash
# Install with NPM
npm install clampography

# Install with PNPM
pnpm add clampography

# Install with Bun
bun install clampography

# Install with Deno
deno install npm:clampography
```

## Usage

```css
/* First import Tailwind CSS */
@import "tailwindcss";

/* Then import Clampography */
@import "clampography";

/* Override default heading styles */
@layer base {
  h1 {
    font-size: clamp(2.35rem, 1.95rem + 1.5vw, 4rem);
    font-weight: 400;
    line-height: 1.15;
  }
}
```
