# 🙌 Clampography

[![npm version](https://img.shields.io/npm/v/clampography)](https://www.npmjs.com/package/clampography)
[![license](https://img.shields.io/npm/l/clampography)](https://github.com/your-username/clampography/blob/main/LICENSE)
[![minzipped size](https://img.shields.io/bundlephobia/minzip/clampography)](https://bundlephobia.com/package/clampography)

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

### The purpose

Tailwind CSS
[resets all default browser styles](https://tailwindcss.com/docs/preflight) to
give you full control. However, writing typography styles from scratch takes
some time. Clampography gives you a quick starting point so you can focus on
more creative tasks.

The heading sizes are very similar to the official Tailwind Typography plugin.
However, some other font sizes might be a bit larger. It is best to visit the
[demo page](https://dav.one/clampography/) to see how it looks.

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

/* Then you can override Clampography's base styles */
@layer base {
  h1 {
    font-size: clamp(2.35rem, 1.95rem + 1.5vw, 4rem);
    font-weight: 400;
    line-height: 1.15;
  }
}
```
