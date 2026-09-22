# Search Dribbble shots

Automatically search Dribbble shots on dribbble.com. Search Dribbble shots by keyword, returning title, url, owner, thumbnail, likes and views for each result.

- Site: dribbble.com
- Address: `reduck/dribbble.com/search_shots`
- Updated: 2026-08-25 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dribbble.com/search_shots`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dribbble.com/search_shots
```

## Input

- `query` (string, required): Search keywords, e.g. "logo design"

## Output

- `results` (array, required)

## FAQ

### What does "Search Dribbble shots" do?

Search Dribbble shots by keyword, returning title, url, owner, thumbnail, likes and views for each result.

### How do I automatically search Dribbble shots on dribbble.com?

Ask an AI agent connected to Reduck to run reduck/dribbble.com/search_shots, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dribbble.com/search_shots

### Is there a dribbble.com API to search Dribbble shots?

You do not need one. "Search Dribbble shots" drives the real dribbble.com pages in a browser, so it works whether or not dribbble.com offers an API for this.

### What information do I need to provide?

Required: query.

### What does it return?

It returns results.

### Do I need to be logged in to dribbble.com?

No. It only uses pages of dribbble.com that are reachable without signing in.

### Does it change anything on dribbble.com, or only read data?

It only reads. It looks things up on dribbble.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dribbble.com/search_shots, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dribbble.com/search_shots

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/dribbble.com/search_shots
