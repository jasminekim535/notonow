# Noto Now · 能登半島の復興へ

A bilingual editorial landing page for **Noto Now**, an architecture and urban
recovery framework for Japan's Noto Peninsula following the January 1, 2024
earthquake. Implemented from the [Now Institute Figma design](https://www.figma.com/design/c0Zpnu8WsTxm70jlmJSWVv/Now-Institute?node-id=394-949).

## Project status & roadmap

### Done so far — Part One
The current site was built by referencing the **Noto publication PDF** stored on
the server. That publication covers **Part One** of the project only: the
disaster context, the recovery framework, the three scales of design (regional
planning → urban design → architectural speculations), and the supporting
research and credits. Everything live today maps to Part One.

### To be done — Part Two (USC students' work)
**Part Two is ongoing** and not yet on the site. It documents the work of the
**USC students**, taking a more *personal* approach to the project than the
framework-driven Part One. As that material is finalized, it should be folded
into the site as follows:

| Tab | What to add |
| --- | --- |
| **About** (`about.html`) | A new section introducing **Part Two / Project 2** — what it is, who is doing it (USC students), and how its personal approach relates to Part One. Follow the existing `.story` card-grid pattern ("Noto Now 1"); a parallel "Noto Now 2" block keeps it consistent. |
| **Design** (`design.html`) | A new section presenting **the work the students created**. Reuse an existing section pattern — the `.spec` slideshow (like Architectural Speculations) or a `.dz-*` block — rather than inventing new layout. |
| **Credits** (`credits.html`) | **Adequate credits** for the Part Two contributors (USC students, advisors, collaborators), following the existing credit-group structure (executive producers / special support / design & editing / research). |

### Requirements for any Part Two additions
- **Design consistency.** Do not introduce new visual language. Reuse the
  existing design tokens (see *Design notes* below) and section patterns. Match
  the eyebrow-kicker → heading → rule → body rhythm used throughout, and the
  full-width max of 1280px.
- **Bilingual (English + 日本語).** Every new piece of copy must ship in both
  languages, using the site's existing conventions:
  - English-only runs of text use `class="t-en"`; Japanese-only runs use
    `class="jp jp-full"`.
  - Eyebrows pair an English label with a JP span: `<span class="kicker__jp">…</span>`.
  - Section headings follow the two-line pattern — English `__h2` plus a JP
    `__h2-jp` sibling — and the JP heading is sized to **~40px** in `mode-jp`
    (see the `body.mode-jp …__h2-jp` rules in `styles.css`) for consistency with
    every other section.
  - Test both languages with the EN / 日本語 toggle before publishing.

## Running

It's a static site — no build step. Open `index.html` directly, or serve it:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Structure

| File | Purpose |
| --- | --- |
| `index.html` | Home page — hero, damage essay, heritage cards, about + framework principles, field documentation, footer |
| `about.html` | About page — About Us section + "Noto Now 1" editorial card grid (the disaster / strategy / approach / goal) |
| `history.html` | History page — "History of Noto" intro with an inline Noto Peninsula map, plus the Earthquake, Cultural economic engines, and Site Images sections |
| `design.html` | Design page — the Foundation intro, three scales of design, challenges, strategies, the "Four Regional Strategies for Ishikawa" map, urban strategies for Wajima, and Architectural Speculations |
| `credits.html` | Publication Credits page — executive producers, special support, design & editing, and urban planning research |
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
