# ON THE RACK — Tech Company Sim

A single-file browser game. Run a tech company, make the calls, live with them.

**Play it:** https://ajhollowayvrm.github.io/tech-company-sim/

## Running locally

There is no build step and no dependencies. Open `index.html` in a browser, or
serve the directory if you prefer a real origin:

```sh
python3 -m http.server
# then visit http://localhost:8000
```

Saves are kept in `localStorage`, so they are per-browser and per-origin — a
local save will not follow you to the deployed site.

## Deployment

`.github/workflows/deploy-pages.yml` publishes the repository root to GitHub
Pages on every push to the default branch.

One-time setup: under **Settings → Pages**, set **Source** to **GitHub
Actions**. The workflow asks to enable Pages itself, but the automatic
`GITHUB_TOKEN` is not allowed to create a Pages site, so the first run fails
with `Resource not accessible by integration` until the source is set by hand.
Once it is set, that step becomes a no-op and deploys run unattended.

`.nojekyll` is present so Pages serves the files as-is rather than running them
through Jekyll.
