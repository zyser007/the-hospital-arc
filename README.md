# The Hospital Arc

A tiny, self-contained **bilingual (EN / TH) novel reader** for the short story
_The Hospital Arc_.

**Live site:** `https://zyser007.github.io/the-hospital-arc/`
_(available once the Pages deploy finishes — see below)_

## What's here

| File | Purpose |
|------|---------|
| `index.html` | The whole reader — HTML, CSS and JS in one file, no build step, no dependencies. |
| `en.txt` / `th.txt` | The raw story in English and Thai. Edit these to change the text. |
| `.github/workflows/deploy-pages.yml` | Deploys the site to GitHub Pages on every push. |

## How it works

`index.html` fetches `en.txt` / `th.txt` at runtime and parses their structure
(section dividers, `DD MONTH — HH:MM` timestamps, `PROLOGUE` / `EPILOGUE`
headings, `— inner thoughts —`, `STATUS EFFECT` badges, all-caps shouts, and
`•` bullet lists) into a styled reading view.

Features: EN/TH language toggle, light/dark theme, reading-progress bar,
scroll-reveal, back-to-top, and remembered preferences — all in ~1 file.

To update the story, just edit `en.txt` / `th.txt` and push; the reader picks
up the changes automatically.

## Enabling GitHub Pages

The included workflow uses `actions/configure-pages` with `enablement: true`,
so it will try to turn Pages on automatically. If your first run reports that
it isn't allowed to deploy, open **Settings → Pages** and set **Source** to
**GitHub Actions**, then re-run the workflow.
