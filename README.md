# Landing Pages

A collection of standalone, self-contained landing pages. Each page lives in its own
folder with a single `index.html` — no build step, no dependencies. Open the file in a
browser to view it.

## Pages

| Page | Folder | Description |
| --- | --- | --- |
| Ember & Origin | [`ember-origin/`](ember-origin/index.html) | Landing page for a specialty coffee roaster whose differentiator is a "story card" naming the farmer behind every bag. Built from the Ember & Origin marketing action plan (positioning, brand pillars, voice, and subscription messaging). |
| Competitive Gap Analysis | [`competitive-analysis/`](competitive-analysis/index.html) | Internal strategy page: Ember & Origin vs. Blue Bottle, Stumptown, and Counter Culture across eight dimensions. Comparison matrix, per-competitor profiles, white-space findings, and a sequenced opportunity backlog. Built from Section 02 of the same plan. |

> **Note:** `competitive-analysis/` is an internal-facing document, not customer-facing marketing.
> If this repo is ever served publicly (e.g. GitHub Pages), consider whether that page should ship with it.

## Conventions

- One folder per page, named in kebab-case.
- Everything inlined in `index.html`: CSS in a `<style>` block, JS in a `<script>` block.
- Web fonts loaded from Google Fonts; no other external dependencies.
- Responsive down to 360px, and `prefers-reduced-motion` is respected.

## Running locally

```bash
# open directly
open ember-origin/index.html

# or serve the whole repo
python3 -m http.server 8000
```
