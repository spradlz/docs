# Documentation project instructions

## About this project

- This is the **HouseLoop** developer documentation site, built on [Mintlify](https://mintlify.com).
- It is published at **houseloop.mintlify.app** from the `spradlz/docs` GitHub repo (`main` branch is the source of truth).
- Pages are MDX files with YAML frontmatter (`title`, `description`). Configuration + navigation live in `docs.json`.
- **Only document what is already deployed and live.** If a feature isn't shipped, it doesn't belong here yet.

## How agents edit these docs

Agents do NOT clone this repo by hand. Use the BossLoop docs tool (it owns clone → write → push):

- MCP tools: `mcp__docs__docs_list`, `docs_read`, `docs_write`, `docs_delete`, `docs_publish`, `docs_status`.
- Or the CLI: `node tools/docs/mintlify-docs.mjs <list|read|write|delete|publish|status>`.

Flow: read the current page → write the full updated MDX → `publish` (commits + pushes to `main` → Mintlify deploys in ~1-2 min). New page = also add its entry to `docs.json` nav.

## Terminology

- Use **HouseLoop** (one word, capital H and L).
- Use "lead" not "contact"; "Run Log" (capitalized) for the operational run feed; "listing" not "property record".

## Style preferences

- Active voice, second person ("you").
- One idea per sentence; keep it concise.
- Sentence case for headings.
- Bold for UI elements: Click **Settings**.
- Code formatting for file names, commands, paths, and code references.

## Content boundaries

- Document live, shipped behavior only — no roadmap or unreleased features.
- Don't document internal agent infrastructure (comms, scrapers, credentials).
