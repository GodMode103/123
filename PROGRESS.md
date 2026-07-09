# Fable 25 — Build Progress & Conventions

**Mission:** 25 fundamentally different websites demonstrating extreme web design
capability, each with a `/guide` route, each receiving ≥3 iteration passes,
deployed publicly with a single hub link. Built autonomously; do not stop to ask
the user anything until all are done.

## Deployment plan
- Higgsfield deploy = unavailable (401 on all calls). Netlify = no credentials.
- **Chosen path:** GitHub Pages on this repo (`godmode103/123`), branch
  `claude/app-ideas-launch-iwotf8`, via `.github/workflows/pages.yml`
  (`actions/configure-pages@v5` with `enablement: true`).
- **Fallback if environment protection blocks non-default branch:** push built
  tree to `gh-pages` branch (classic auto-enable). Note to user afterward.
- Expected URL: `https://godmode103.github.io/123/`

## Repo layout (pure static, no build step)
- `index.html` — hub gallery linking all 25 sites (build LAST)
- `guide/index.html` — root methodology guide
- `s/<slug>/index.html` — each site, fully self-contained (inline CSS/JS)
- `s/<slug>/guide/index.html` — per-site guide: concept, techniques, iteration log
- `.nojekyll` — required so Pages serves everything verbatim

## Hard conventions (every site)
- ALL links relative (hosted under `/123/` subpath)
- Self-contained: inline CSS/JS; Google Fonts CDN allowed; no other CDNs unless
  necessary (three.js not used — all 3D/shader work is raw WebGL/canvas/CSS)
- Inline SVG data-URI favicon, `<title>`, meta description
- `prefers-reduced-motion` respected with static fallback
- Responsive to 360px; no horizontal body scroll
- Discreet footer/corner links: "⌂ Fable 25" → `../../` and "Guide" → `guide/`
- Distinct palette + type pairing per site — NO two sites may share a vibe
- Iteration passes: P1 build → P2 fine-tooth comb (contrast, spacing, overflow,
  dead zones, motion quality) → P3 complexify + polish (a11y, mobile,
  reduced-motion, one extra flourish). Log all three in the site's guide.

## Roster & status
| # | slug | concept / signature technique | P1 | P2 | P3 |
|---|------|-------------------------------|----|----|----|
| 01 | onsen | Japanese ryokan; sumi-e ink canvas, vertical text, steam | | | |
| 02 | heliosphere | Raw WebGL2 raymarched sun/plasma shader hero | | | |
| 03 | terminal-romance | CRT phosphor terminal; typed love letters | | | |
| 04 | brutal-post | Brutalist broadsheet; massive type, harsh grid | | | |
| 05 | porcelain | Claymorphic ceramic studio; soft 3D pastel | | | |
| 06 | midnight-atelier | Luxury fashion house; horizontal scroll gallery | | | |
| 07 | signalform | Swiss International Style bureau; strict grid | | | |
| 08 | chromatic-field | Generative flow-field art gallery; regenerable | | | |
| 09 | deep-current | Ocean descent scroll story; parallax depth | | | |
| 10 | papercut | CSS-3D layered paper theater storybook | | | |
| 11 | neon-district | Cyberpunk arcade; canvas rain, glitch type | | | |
| 12 | herbarium | Botanical archive; engraved SVG specimens | | | |
| 13 | orbital | Space telemetry dashboard; live canvas orbits | | | |
| 14 | velvet-lounge | Art-deco jazz club; gold geometry, visualizer | | | |
| 15 | concrete-poetry | Kinetic typography; cursor-reactive words | | | |
| 16 | glacier | Polar expedition; frosted glassmorphism | | | |
| 17 | bazaar-of-hours | Otherworldly clock market; animated SVG clocks | | | |
| 18 | pixels-and-plunder | 8-bit game studio; CSS pixel art sprites | | | |
| 19 | aureate | Sacred geometry meditation; breathing golden ratio | | | |
| 20 | static-and-bloom | Vaporwave Y2K; chrome text, checkered floor | | | |
| 21 | the-ledger | Editorial broadsheet longread; fine typography | | | |
| 22 | mono-no-aware | Falling petal particle poem; seasons | | | |
| 23 | frequency | WebAudio synth lab; oscilloscope (user-gated audio) | | | |
| 24 | cartographer | Pannable hand-drawn SVG map explorer | | | |
| 25 | ascii-garden | Living ASCII ecosystem in a `<pre>` | | | |

Mark passes with ✓ as completed. Update this file as work proceeds — it is the
source of truth across context compactions.
