# 🙌 Clampography

**Clampography** is a CSS-only alternative to the official
[Tailwind CSS Typography plugin](https://github.com/tailwindlabs/tailwindcss-typography).
Instead of fixed sizes, it uses the CSS
[clamp()](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Values/clamp)
function to create fluid typography that adapts to any screen. With
[94% global browser support](https://caniuse.com/css-math-functions), it works
on nearly all devices.

Designed for [Tailwind v4's](https://tailwindcss.com/blog/tailwindcss-v4)
CSS-first system, no JavaScript configuration needed. Best suited for simple
websites like blogs and articles.

## Philosophy

**Clampography** is built on three core principles to match
`@tailwindcss/typography` quality standards while remaining pure CSS:

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

# Install with Deno
deno install npm:clampography

# Install with Bun
bun install clampography
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
    letter-spacing: 0.05em;
  }
}
```
