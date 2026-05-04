# Casa Arbre × Gustaf Westman — Pop-up deck

Single-page scroll-based lookbook. Cocoon brand-aligned. Drops directly to GitHub Pages.

## What's here

```
casa-arbre-gustaf/
├── index.html              ← the deck (single self-contained page)
├── img/
│   ├── arbre/              ← 13 cafe + listening room photos
│   ├── apartment/          ← 12 top-floor residence photos
│   └── plans/              ← 2 floorplans (not currently shown — available if needed)
├── deploy.sh               ← one-command deploy to GitHub Pages
└── README.md               ← this file
```

## Preview locally

```bash
# from this folder:
open index.html
```

It's a static page — no server needed.

## Deploy to GitHub Pages

```bash
# from this folder:
bash deploy.sh
```

Prerequisites: `gh` CLI authenticated (`brew install gh && gh auth login`).

The script will:
1. Init a git repo here
2. Create a new repo on your GitHub account (you pick the name — defaults to `cocoon-gustaf-westman-pop-up`)
3. Push the deck
4. Enable Pages
5. Print the live URL

Pages takes 30–90 seconds to build the first time.

## What needs Eduard's review before sending

Three things I couldn't finalize from the sandbox — quick swaps:

### 1. Gustaf's furniture imagery (currently stylized SVGs)

Each Zone (Café / Listening Room / Residence) has a "mood" block with four pieces of Gustaf's work alongside a Casa Arbre photo. They're currently stylized terracotta SVGs evoking his iconic chunky/curvy aesthetic. They look intentional, not like placeholders — but to elevate the proposal, swap them for real product photography from gustafwestman.com.

To swap: drop product PNGs (white or transparent background, ~600px) into `img/gustaf/` and replace the inline `<svg>` blocks in `index.html` with `<img src="img/gustaf/curvy-mirror.png" alt="...">`. The 12 SVG slots are clearly labeled by zone in the HTML — search for `furniture-item` in the file.

### 2. Apartment shot identification

The apartment photos came from the Drive owner folder with UUID filenames. I named them by what's visible:

| File | Shows |
|---|---|
| `living-room.jpg` | Bright living with white-brick wall + blue sofa |
| `living-armchair.jpg` | Tan armchair detail |
| `dining-table.jpg` | Long wooden dining table, lots of natural light |
| `open-kitchen-stairs.jpg` | Open kitchen + stairs with skylight |
| `kitchen-detail.jpg` | Kitchen counter w/ terracotta tile (very Cocoon!) |
| `bedroom-loft.jpg` | Attic-style bedroom, green/teal headboard |
| `bedroom-blue.jpg` | Blue striped bedroom |
| `bedroom-floral.jpg` | Bedroom w/ floral linens |
| `bathroom-tub.jpg` | Master bath with tub |
| `bathroom-sink.jpg` | Bath sink area |
| `bathroom-shower.jpg` | Shower stall |
| `garden-patio.jpg` | Rear garden patio with greenery |

The deck currently uses 7 of these. Swap any in `index.html` if you want different shots featured.

### 3. Pricing line items

Sanity-check that the three options match what you've quoted before:
- Option A — $25K + Casa Manager + Cleaning · café operates · marketing collab
- Option B — $27K + Casa Manager + Cleaning · all of A + Reforesters sound programming (your team approves)
- Option C — $40K + Casa Manager + Cleaning · café closed, programming paused

Edit in the `<!-- PRICING -->` section of `index.html`.

## Brand specs used

- Hero colors: `#F54029` (Brilliance / terracotta) + `#F5F2E8` (Natural / cream)
- Accent: `#275453` (Clarity / deep teal)
- Type: Helvetica Neue (Bold for titles, Medium for headlines, Regular for body)
- Tone: cheerful, confident, conversational — first person from Eduard, per the brief

Aligned with the Cocoon Brand Guide v1.0 (Feb 2023) and the Casa Arbre wiki (`casa-arbre.md` in Drive).
