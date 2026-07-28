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
Pages on every push to the default branch. The first successful run enables
Pages itself; no manual setup is required in repository settings.

`.nojekyll` is present so Pages serves the files as-is rather than running them
through Jekyll.
