# Landing Pages

A collection of standalone, self-contained pages. Each lives in its own folder with a
single `index.html` — no build step, no dependencies. Open the file in a browser to view it.

## Pages

| Page | Folder | Published? | Description |
| --- | --- | --- | --- |
| Marketing Action Plan | [`docs/`](docs/index.html) | **Yes — GitHub Pages** | The full six-section strategy document the other two pages are derived from: positioning, competitive gap, a 4-week content calendar, five acquisition strategies, three quick wins, and 30-day success metrics. |
| Ember & Origin | [`ember-origin/`](ember-origin/index.html) | No | Landing page for a specialty coffee roaster whose differentiator is a "story card" naming the farmer behind every bag. Built from the plan's positioning, brand pillars, voice, and subscription messaging. |
| Competitive Gap Analysis | [`competitive-analysis/`](competitive-analysis/index.html) | No | Internal strategy page: Ember & Origin vs. Blue Bottle, Stumptown, and Counter Culture across eight dimensions. Comparison matrix, per-competitor profiles, white-space findings, and a sequenced opportunity backlog. Built from Section 02 of the plan. |

## Publishing

GitHub Pages serves **`docs/` only**, from the `main` branch. Live at:

> https://ahgaoh83.github.io/Landing-Pages/

Pages can only serve the repo root or a `/docs` folder — not an arbitrary subfolder — so the
marketing plan lives in `docs/` to keep it the single published page. `ember-origin/` and
`competitive-analysis/` remain in the repo as source but get no public URL.

**Anything added to `docs/` becomes publicly viewable.** Everything else in the repo is still
readable on github.com (the repo is public), just not rendered as a webpage. If that distinction
matters, make the repo private — the Pages site stays reachable only on a paid plan, so check
before relying on it.

`docs/.nojekyll` disables the Jekyll build so files are served exactly as committed.

## Provenance

`docs/index.html` is the original marketing plan document, essentially verbatim. Two changes:

- A one-line mobile fix — `body { flex-direction: column }` under 900px, without which the
  full-width sidebar pushed the content column ~116px off-screen on phones.
- The sidebar's "Related pages" links were removed, since their targets aren't published and
  would 404 for anyone visiting the Pages site.

## Conventions

- One folder per page, named in kebab-case.
- Everything inlined in `index.html`: CSS in a `<style>` block, JS in a `<script>` block.
- Web fonts loaded from Google Fonts; no other external dependencies.
- Responsive down to 360px, and `prefers-reduced-motion` is respected.

## Running locally

```bash
# open directly
open docs/index.html

# or serve the whole repo
python3 -m http.server 8000
```
