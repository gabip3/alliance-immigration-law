# Alliance Immigration Law

Website concept for Alliance Immigration Law, a trilingual immigration practice based in Marietta, Georgia.

Single-page static site. No build step, no dependencies, no framework. Open `index.html` in a browser and it runs.

## Structure

```
index.html              the whole site (markup, styles and script inline)
assets/logo-mark.png    brand symbol, cropped from the firm's logo
assets/logo-full.png    full logo lockup, symbol plus wordmark
assets/renata.webp      attorney portrait
```

## What it does

- **Trilingual.** The EN / PT / ES switch in the header retranslates the entire page from a dictionary in the script: headings, all nine practice areas, memberships, form placeholders and the select options. No page reload.
- **Custom icon set.** The nine practice-area icons are hand-drawn inline SVG in a single monoline style. Every shape carries `pathLength="1"`, so on hover each icon redraws stroke by stroke at a uniform speed regardless of the real path length, and shifts from brand blue to pale blue.
- **Portrait treatment.** The attorney photo has a plain white studio background. Instead of cutting it out, the image sits on a pale blue panel with `mix-blend-mode: multiply`, so the white dissolves and the figure integrates with no halo.
- **Motion.** Scroll progress bar, header that solidifies past the fold, staggered reveal on scroll, a headline word that cycles, a hero gradient that follows the cursor, an infinite practice-area ticker, and a pulsing WhatsApp button fixed to the corner.
- **Responsive.** Three-column grid down to a single column, verified with no horizontal overflow from 1440px to 375px.
- **Accessible-ish.** Honours `prefers-reduced-motion` by disabling every animation and revealing all content immediately.

## Typography and colour

Montserrat for headings, buttons and labels, matching the wordmark in the logo. Inter for body copy.

The palette is sampled directly from the logo file:

| Token | Value | Use |
| --- | --- | --- |
| `--brand` | `#2f68f7` | primary blue, from the logo symbol |
| `--brand-l` | `#68a8f8` | mid blue |
| `--sky` | `#88d0f0` | pale blue accent |
| `--ice` | `#b0e8f0` | lightest tint |
| `--navy-d` | `#061128` | footer and ticker |

## Known limitations

- **The contact form is a mockup.** Submitting it fires an `alert()`. It needs to be wired to a CRM or an email service before going live.
- **The portrait is 564x540**, which is the largest version available on the current site. It is adequate for the space it occupies but would benefit from a higher-resolution original, especially on retina screens.
- Fonts load from Google Fonts, the only external request the page makes.
