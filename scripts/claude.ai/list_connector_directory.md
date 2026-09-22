# List connector Claude directory

Automatically list connector Claude directory on claude.ai. Every connector in Claude's Directory (Settings → Connectors → Add → Browse connectors) — the whole catalogue the page loads, not one page. Each entry carries id, slug, name, one-liner, verified tier (anthropic/partner/community), categories, author, its claude.ai/directory link and the MCP endpoint URL. The Directory's Plugins tab (local extensions) is a different affordance and is not returned.

- Site: claude.ai
- Address: `reduck/claude.ai/list_connector_directory`
- Updated: 2026-08-26 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/claude.ai/list_connector_directory`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/claude.ai/list_connector_directory
```

## Input

It takes no input.

## Output

- `total` (integer, required): How many connectors the Directory lists — equals connectors.length.
- `connectors` (array, required): Every connector in the Directory's Connectors tab, in the order the feed returns them (the order the grid renders). Never empty: an empty Directory is a broken read, not a state the site has.

## FAQ

### What does "List connector Claude directory" do?

Every connector in Claude's Directory (Settings → Connectors → Add → Browse connectors) — the whole catalogue the page loads, not one page. Each entry carries id, slug, name, one-liner, verified tier (anthropic/partner/community), categories, author, its claude.ai/directory link and the MCP endpoint URL. The Directory's Plugins tab (local extensions) is a different affordance and is not returned.

### How do I automatically list connector Claude directory on claude.ai?

Ask an AI agent connected to Reduck to run reduck/claude.ai/list_connector_directory, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/list_connector_directory

### Is there a claude.ai API to list connector Claude directory?

You do not need one. "List connector Claude directory" drives the real claude.ai pages in a browser, so it works whether or not claude.ai offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns total, connectors.

### Do I need to be logged in to claude.ai?

Yes. It acts as you on claude.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the claude.ai cookies saved by the Reduck extension.

### Does it change anything on claude.ai, or only read data?

It only reads. It looks things up on claude.ai and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/claude.ai/list_connector_directory, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/list_connector_directory

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/claude.ai/list_connector_directory
