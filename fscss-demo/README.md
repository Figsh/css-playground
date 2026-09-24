# FSCSS Demo Project (2026)

A minimal static site demonstrating **FSCSS** (Figured Shorthand Cascading Style Sheets) v1.2.4.

## What’s included

- `index.html` — page structure + FSCSS runtime via CDN
- `styles.fscss` — styles written with FSCSS features:
  - Variables (`$primary`, `$radius`, …)
  - Design-token store (`@fun(tokens)`)
  - Color array (`@arr colors[...]`)
  - Reusable mixins (`@define flex-center()`, `@define card-base()`)
  - Array access for color swatches
  - Normal CSS intermixed

## How to run (browser / live)

1. Open `index.html` in a modern browser  
   (or serve the folder with any static server).

The CDN script (`runtime.min.js`) automatically finds the `<link type="text/fscss">` and compiles the FSCSS on the fly.

```html
<script src="https://cdn.jsdelivr.net/npm/fscss@1.2.4/runtime.min.js" defer></script>
<link type="text/fscss" href="styles.fscss">
```

## Production build (recommended)

Install the CLI and compile to plain CSS:

```bash
npm install -g fscss@1.2.4   # or locally
fscss styles.fscss styles.css
```

Then replace the link in `index.html` with a normal stylesheet:

```html
<link rel="stylesheet" href="styles.css">
```

(No runtime script needed.)

## Key FSCSS features used

| Feature          | Example in this project                  |
|------------------|------------------------------------------|
| Variables        | `$primary: #2563eb;`                     |
| @fun store       | `@fun(tokens) { space-lg: 2rem; }`       |
| @define mixin    | `@define card-base() { … }`              |
| Arrays           | `@arr colors[#2563eb, …]`                |
| Array access     | `background: @arr.colors[0];`            |

## Links

- Docs: https://fscss.devtem.org/
- npm: https://www.npmjs.com/package/fscss
- GitHub: https://github.com/fscss-ttr/FSCSS

Enjoy styling with less boilerplate!
