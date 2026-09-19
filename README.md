# DashSquad docs

Source for the DashSquad user documentation at **[docs.dashsquad.ai](https://docs.dashsquad.ai)**, built with [Mintlify](https://mintlify.com).

This repo is mounted as the `docs/` submodule of [volumegambit/Dash](https://github.com/volumegambit/Dash). Page content lives here; the Dash repo only pins a commit of it.

## Structure

- `docs.json` — site config: theme, colors, and the navigation tree. A page only appears on the site once it is listed here.
- `*.mdx` — one file per page, with `title` and `description` frontmatter. The file name (without `.mdx`) is the page slug.

## Preview locally

```bash
npm i -g mint
mint dev
```

Run `mint dev` from the repo root (where `docs.json` is) and open `http://localhost:3000`. Run `mint broken-links` before pushing to catch dead internal links.

## Publishing

The Mintlify GitHub app deploys every push to `main` to docs.dashsquad.ai. There is no separate release step.

## Editing from the Dash repo

```bash
cd docs
# edit pages, then:
git add <files> && git commit -m "docs: ..." && git push
cd ..
git add docs && git commit -m "chore(docs): bump docs submodule"
```

Push here first, then commit the new `docs` pointer in Dash. Dash's CI runs tests against the pinned commit, so a docs change that a feature depends on needs both commits.

`plans/` and `superpowers/` are Dash's private dev-plan directories. They sit inside this checkout when it is used as the submodule, and are ignored by both git and Mintlify.
