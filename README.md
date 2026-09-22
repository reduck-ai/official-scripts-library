# Reduck official script library

A mirror of the public script catalogue at [reduck.ai](https://reduck.ai/explore/scripts). 905 scripts,
one markdown document each, under `scripts/<site>/<script>.md`. Each document is the same one the
site serves at its page's address plus `.md`, so this repository and the site never disagree.

A **script** is a browser automation for one site, addressed as `@reduck/<site>/<slug>`. It drives
the real page, so it works on sites with no API and on pages behind a login, and it answers JSON
matching a declared output schema. Each document says what a script takes, what it returns, and how
to run it.

## Running one

From an agent connected over MCP at `https://mcp.reduck.ai/mcp`, ask for the script by address.
From a terminal:

```bash
npx @reduck-ai/cli@latest run --script @reduck/luma.com/get_event_attendees
```

A script runs on a Chrome you have paired, where you are already signed in, or on a Reduck-hosted
browser.

## What is here

- `scripts/<site>/<slug>.md` — one document per script.
- `index.json` — every script with its address, its page and the date it last changed.

## Keeping it current

A daily job reads the catalogue and commits the documents that changed. Edits made here are
overwritten on the next run: the source of truth is [reduck.ai](https://reduck.ai).
