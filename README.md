# Noto Now · 能登半島の復興へ

A bilingual editorial landing page for **Noto Now**, an architecture and urban
recovery framework for Japan's Noto Peninsula following the January 1, 2024
earthquake. Implemented from the [Now Institute Figma design](https://www.figma.com/design/c0Zpnu8WsTxm70jlmJSWVv/Now-Institute?node-id=394-949).

## Running

It's a static site — no build step. Open `index.html` directly, or serve it:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Structure

| File | Purpose |
| --- | --- |
| `index.html` | Page markup — hero, damage essay, heritage cards, about + framework principles, field documentation, footer |
| `styles.css` | All styling (design tokens, layout, responsive breakpoints) |

## Design notes

- **Palette:** ink `#1b1f2a`, warm paper `#eceae5`, stone `#d8d4ce`, accent red `#7d3535`
- **Type:** Cormorant Garamond (display serif), Inter (sans), Noto Serif JP / Shippori Mincho B1 (Japanese), loaded from Google Fonts
- **Layout:** 1280px max content width, responsive down to mobile (grids collapse to single column)

## Images

Image `src` values are wired up in the inline `IMAGES` map at the bottom of
`index.html`, currently pointing at the **temporary Figma export URLs** from the
design. These are short-lived — for production, export the assets and replace the
URLs (keyed by `data-img`) with permanent paths. Each `<img>` has an `onerror`
fallback so the layout degrades gracefully to its background tone if an image
fails to load.
