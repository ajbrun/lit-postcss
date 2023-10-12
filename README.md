# Repository to demonstrate lit/postcss issue
This repository highlights an issue attempting to get postcss to work with web component CSS under the shadow dom. Autoprefixer has been installed using default settings, with the expectation that the CSS property `columns` should have prefixes applied.

**What works:** Global CSS styles. Example in `/src/index.css` in `columns: 5;` on `body` tag
**What doesn't work:** Component CSS styles. Example in `/src/my-element.ts`

## How to run
``` bash
npm i
npm run dev
```

When inspecting the body tag, the global CSS has prefixes applied. However, when inspecting the `my-element` tag, the same is not the case.

Question: How can postcss plugins be applied to the inline lit styles?