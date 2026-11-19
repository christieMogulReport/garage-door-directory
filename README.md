# Garage Door Fix Finder

Static directory site (Python + Markdown) planned for https://garagedoor.christiejustice.com via GitHub Pages. Brand: Black Swan Sibyl.

**Status: not yet deployed.** No git remote exists yet; nothing has been pushed. Don't create a GitHub repo or push until Christie approves.

## Commands
```bash
python3 build.py            # build into dist/ (drafts excluded)
python3 serve.py            # build and preview at http://127.0.0.1:8000
python3 build.py --drafts   # include draft: true pages
```
The first run creates a local `.venv` and installs `requirements.txt`.

## Add a page
Create `content/pages/<slug>.md` with front matter: `title`, `slug`, `description`, `last_updated` (YYYY-MM-DD), optional `draft`, optional `listings` (each with `name`, `url`, optional `affiliate_url`, `summary`, `category`). Quote any value containing a colon. Homepage intro is `content/home.md`; site settings are `config.yml`.

## Rules for content
- Only real, sourced information. Every cost figure, safety claim, or stat must come from a source that was actually fetched; link it. If a number can't be sourced, leave it out. Say "call to confirm" for prices.
- Safety first: never encourage DIY work on torsion springs or cables.
- Before adding an affiliate link, fill `affiliate_disclosure` in `config.yml`.

## Deploy (not set up yet)
Once a remote exists: push to `main`; `.github/workflows/pages.yml` builds and deploys to GitHub Pages. `static/CNAME` holds the custom domain.
`data/` and `tools/` are gitignored (private earnings and outreach notes).
