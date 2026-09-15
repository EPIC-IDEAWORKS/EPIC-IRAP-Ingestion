# Mohawk College Brand Style Guide
*Condensed reference for web development — extracted from Mohawk College Brand Identity Guidelines (Updated November 2023)*

## Colours

### Primary Palette

| Name | HEX | RGB | CMYK | Pantone |
|------|-----|-----|------|---------|
| Charcoal | `#333333` | R51 G51 B51 | 15Y 82K | PMS Black 7 |
| Burgundy | `#660033` | R102 G0 B51 | 100M 30Y 61K | PMS 7421 |
| Crimson | `#990033` | R153 G0 B51 | 100M 63Y 29K | PMS 201 |
| Orange | `#ff9933` | R255 G153 B51 | 60M 100Y | PMS 158 |

**Usage notes:**
- Charcoal is used for the wordmark/body text (grey-charcoal tone).
- Burgundy, Crimson, and Orange are the three "pillar" colours used in the logo symbol (representing Quality, Innovation, Sustainability).
- Section/divider backgrounds in official materials use full-bleed Burgundy, Crimson, or Orange blocks with white text.
- On dark backgrounds, use white or reversed (light) versions of text/logo elements — white and light-on-dark are preferred over full-colour-on-black for most content, though a charcoal logo on solid black is acceptable for subtle effects.

### Suggested CSS custom properties
```css
:root {
  --mohawk-charcoal: #333333;
  --mohawk-burgundy: #660033;
  --mohawk-crimson: #990033;
  --mohawk-orange: #ff9933;
  --mohawk-white: #ffffff;
}
```

## Typography

- **Primary typeface:** Verdana (Regular, Italic, Bold, Bold Italic). Chosen for accessibility/legibility; standard and widely available across web, print, and digital.
- **Logotype-only font:** The "Mohawk" logotype itself is a custom wordmark based on House Movements Runway (modified) — this is for the logo graphic only, not for general body/heading text.
- For a simple website, use **Verdana** (or a similar accessible sans-serif fallback stack) as the primary font for body copy and headings.

```css
body {
  font-family: Verdana, Geneva, sans-serif;
}
```

## Brand Essence / Tone

- Tagline: **"Future Ready"** — can pair with the logo, always in one of the four corporate colours or white (on a reversed/dark logo).
- Brand pillars: **Quality, Innovation, Sustainability** (represented by the three coloured bars in the logo symbol).
- Voice/positioning themes: confident, excited, optimistic; focused on health and technology as growth areas; community-oriented; forward-looking ("Future Ready").

## Logo Usage (if incorporating the Mohawk logo)

- The wordmark must always appear **with** the symbol (three coloured bars) — never alone.
- Do not recolour, distort, rearrange, or resize logo elements independently.
- Maintain clear space around the logo equal to the width of the "M" symbol.
- Minimum logo height: 0.125 in.
- On dark backgrounds, use the white/reverse version of the logo.

## General Style Takeaways for a Simple Site

- **Palette:** Charcoal text/neutrals, with Burgundy/Crimson/Orange as accent colours for headers, buttons, links, or section dividers.
- **Typography:** Clean, accessible sans-serif (Verdana or equivalent), no decorative fonts for body text.
- **Layout feel:** Bold, confident colour blocks (seen throughout the guideline deck as full-bleed section dividers) with generous white space elsewhere.
- **Tone:** Optimistic, modern, straightforward — avoid cluttered or "busy" backgrounds behind key brand elements.

---
*Source: Mohawk College Brand Identity Guidelines, updated November 2023. For official logo files or further brand guidance, contact Marketing and Creative Services.*
