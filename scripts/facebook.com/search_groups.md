# Find Facebook groups by keyword

Automatically find Facebook groups by keyword on facebook.com. Find Facebook groups by keyword with member counts and posting activity, as structured data. Search Facebook groups by keyword. Returns groupId, name, url, privacy, members, postsPerDay. Results are infinite-scroll, capped by limit.

- Site: facebook.com
- Address: `reduck/facebook.com/search_groups`
- Updated: 2026-09-19 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/facebook.com/search_groups`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/facebook.com/search_groups
```

## Input

- `query` (string, required): Free-text search, e.g. "automatisation IA".
- `limit` (integer, optional): Max groups to return. The page is infinite-scroll; the script scrolls until it has this many cards or the list is exhausted.

## FAQ

### What does "Find Facebook groups by keyword" do?

Find Facebook groups by keyword with member counts and posting activity, as structured data. Search Facebook groups by keyword. Returns groupId, name, url, privacy, members, postsPerDay. Results are infinite-scroll, capped by limit.

### How do I automatically find Facebook groups by keyword on facebook.com?

Ask an AI agent connected to Reduck to run reduck/facebook.com/search_groups, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/search_groups

### Is there a facebook.com API to find Facebook groups by keyword?

You do not need one. "Find Facebook groups by keyword" drives the real facebook.com pages in a browser, so it works whether or not facebook.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: limit.

### Do I need to be logged in to facebook.com?

Yes. It acts as you on facebook.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the facebook.com cookies saved by the Reduck extension.

### Does it change anything on facebook.com, or only read data?

It only reads. It looks things up on facebook.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/facebook.com/search_groups, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/search_groups

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/facebook.com/search_groups
