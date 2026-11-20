# List Wayback Machine snapshots of a page

Automatically list Wayback Machine snapshots of a page on archive.org. List the Wayback Machine captures of a web page (or of a whole site with match type prefix or domain), oldest first, optionally between two dates and with identical captures collapsed. Each capture has its timestamp, original URL, MIME type, HTTP status and a link to view it. An empty list means no capture in that range. Use limit and offset to page.

- Site: archive.org
- Address: `reduck/archive.org/list_wayback_snapshots`
- Updated: 2026-11-19 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/archive.org/list_wayback_snapshots`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/archive.org/list_wayback_snapshots
```

## Input

- `url` (string, required)
- `to` (string, optional): Latest date, YYYY to YYYYMMDDhhmmss.
- `from` (string, optional): Earliest date, YYYY to YYYYMMDDhhmmss.
- `limit` (integer, optional)
- `offset` (integer, optional)
- `match_type` (string, optional): exact = this URL only; prefix = every URL under this path; host = the whole host; domain = host and subdomains.
- `collapse_identical` (boolean, optional): Skip captures whose content is identical to the previous one.

## Output

- `snapshots` (array, required)

## FAQ

### What does "List Wayback Machine snapshots of a page" do?

List the Wayback Machine captures of a web page (or of a whole site with match type prefix or domain), oldest first, optionally between two dates and with identical captures collapsed. Each capture has its timestamp, original URL, MIME type, HTTP status and a link to view it. An empty list means no capture in that range. Use limit and offset to page.

### How do I automatically list Wayback Machine snapshots of a page on archive.org?

Ask an AI agent connected to Reduck to run reduck/archive.org/list_wayback_snapshots, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/archive.org/list_wayback_snapshots

### Is there a archive.org API to list Wayback Machine snapshots of a page?

You do not need one. "List Wayback Machine snapshots of a page" drives the real archive.org pages in a browser, so it works whether or not archive.org offers an API for this.

### What information do I need to provide?

Required: url. Optional: to, from, limit, offset, match_type, collapse_identical.

### What does it return?

It returns snapshots.

### Do I need to be logged in to archive.org?

No. It only uses pages of archive.org that are reachable without signing in.

### Does it change anything on archive.org, or only read data?

It only reads. It looks things up on archive.org and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/archive.org/list_wayback_snapshots, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/archive.org/list_wayback_snapshots

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/archive.org/list_wayback_snapshots
