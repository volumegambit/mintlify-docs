# Documentation project instructions

## About this project

- User documentation for [Dash](https://github.com/volumegambit/Dash), published at https://docs.dashsquad.ai
- Built on [Mintlify](https://mintlify.com). Pages are MDX files with YAML frontmatter (`title`, `description`)
- Configuration and navigation live in `docs.json` — add every new page to the navigation there
- This repo is the `docs/` submodule of the Dash repo. After pushing here, the Dash repo needs its `docs` pointer bumped
- Preview with `mint dev`; check links with `mint broken-links`

## Terminology

- **DashSquad** — the product name on this site (`name` in `docs.json`). Some pages still say "Dash"; use DashSquad in new titles and copy.
- **Mission Control** — the desktop app. Always capitalized.
- **gateway** — the background service that runs agents. Lowercase in running text.
- **agent** / **squad member** — an AI agent the user runs. The user's set of agents is their **squad**.
- **sub-agent** — a helper an agent starts to take part of a job.

## Style preferences

- Use active voice and second person ("you")
- Keep sentences concise — one idea per sentence
- Use sentence case for headings
- Bold for UI elements: Click **Settings**
- Code formatting for file names, commands, paths, and code references

## Content boundaries

- **User-facing only.** Document how to set up, configure, and use Dash.
- Do not document developer-facing details: CI, internal tooling, contribution workflows, linter configs, or internal architecture that users never touch.
- Never commit anything under `plans/` or `superpowers/` — those are Dash's private dev-plan directories and are gitignored here.
