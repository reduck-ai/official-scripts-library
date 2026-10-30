# List connector Claude directory

Automatically list connector Claude directory on claude.ai. One page of the connectors in Claude's Directory (Settings → Connectors → All connectors), 48 at a time in the order the grid shows them. Each entry carries id, slug, name, one-liner, full description, verified tier (anthropic/partner/community), categories, publisher, icon, the MCP endpoint URL and the date it joined. Pass the returned next_cursor to read the next page; it is null on the last page. A cursor the Directory refuses is reported as such. The Plugins tab and your own custom connectors are not returned.

- Site: claude.ai
- Address: `reduck/claude.ai/list_connector_directory`
- Updated: 2026-10-29 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/claude.ai/list_connector_directory`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/claude.ai/list_connector_directory
```

## Input

- `cursor` (string, optional): next_cursor from a previous call, to read the next page. Omit for the first page.

## Output

- `connectors` (array, required): One page of the Directory's All connectors view, in the order the grid shows them (48 per page; the last page can hold fewer). Never empty: an empty page is a broken read.
- `next_cursor` (string | null, required): Pass as cursor to read the next page; null on the last page.

## FAQ

### What does "List connector Claude directory" do?

One page of the connectors in Claude's Directory (Settings → Connectors → All connectors), 48 at a time in the order the grid shows them. Each entry carries id, slug, name, one-liner, full description, verified tier (anthropic/partner/community), categories, publisher, icon, the MCP endpoint URL and the date it joined. Pass the returned next_cursor to read the next page; it is null on the last page. A cursor the Directory refuses is reported as such. The Plugins tab and your own custom connectors are not returned.

### How do I automatically list connector Claude directory on claude.ai?

Ask an AI agent connected to Reduck to run reduck/claude.ai/list_connector_directory, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/list_connector_directory

### Is there a claude.ai API to list connector Claude directory?

You do not need one. "List connector Claude directory" drives the real claude.ai pages in a browser, so it works whether or not claude.ai offers an API for this.

### What information do I need to provide?

Optional: cursor.

### What does it return?

It returns connectors, next_cursor.

### Do I need to be logged in to claude.ai?

Yes. It acts as you on claude.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the claude.ai cookies saved by the Reduck extension.

### Does it change anything on claude.ai, or only read data?

It only reads. It looks things up on claude.ai and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/claude.ai/list_connector_directory, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/list_connector_directory

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/claude.ai/list_connector_directory
