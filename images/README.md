# Images

This folder holds the photography for the page. The files here are currently
**labelled placeholders** — replace any of them with a real photo using the
**same filename** and it will appear on the site automatically (no code change
needed). The mapping lives in the `IMAGES` object near the bottom of
`../index.html`, keyed by each `<img data-img="…">`.

| File | Used for | Suggested size (w × h) |
| --- | --- | --- |
| `hero.jpg` | Hero background + damage mosaic (tall) — structural collapse, Wajima city centre | ~1600 × 1000 |
| `fire.jpg` | Damage mosaic — fire aftermath | ~760 × 600 |
| `urban.jpg` | Damage mosaic — urban damage / landslides | ~760 × 600 |
| `empty.jpg` | Damage mosaic — empty streets / flooding | ~760 × 520 |
| `coastal.jpg` | Damage mosaic — coastal damage | ~760 × 520 |
| `nuri.jpg` | Heritage card 01 — Wajima-nuri | ~920 × 740 |
| `market.jpg` | Heritage card 02 — the morning market | ~920 × 740 |
| `kiriko.jpg` | Heritage card 03 — Kiriko Festival | ~920 × 740 |
| `about.jpg` | About section — traditional joinery, Wajima townhouse | ~1120 × 800 |
| `remapping.jpg` | Documentation — coastal remapping | ~600 × 440 |
| `survey.jpg` | Documentation — street-level survey | ~600 × 440 |
| `workshop.jpg` | Documentation — workshop documentation | ~600 × 440 |
| `aerial.jpg` | Documentation — aerial survey grids | ~600 × 440 |

Images are rendered with `object-fit: cover`, so exact dimensions don't matter —
just match the rough aspect ratio. If you prefer a different format (e.g. `.webp`),
update the corresponding path in the `IMAGES` map in `index.html`.
