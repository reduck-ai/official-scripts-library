# Search ComeUp freelancers

Automatically search ComeUp freelancers on comeup.com. Search ComeUp sellers/freelancers by keyword. Returns username, display name, verified badge and avatar for each match (ComeUp's seller-search results are minimal — use get_profile with the returned username for headline, bio, stats, portfolio and services).

- Site: comeup.com
- Address: `reduck/comeup.com/search_freelancers`
- Updated: 2026-08-25 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/comeup.com/search_freelancers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/comeup.com/search_freelancers
```

## Input

- `query` (string, required): Free-text keyword, e.g. "seo" or "logo design"

## Output

- `total` (integer | null, optional): Total sellers matching the query
- `freelancers` (array, optional)

## FAQ

### What does "Search ComeUp freelancers" do?

Search ComeUp sellers/freelancers by keyword. Returns username, display name, verified badge and avatar for each match (ComeUp's seller-search results are minimal — use get_profile with the returned username for headline, bio, stats, portfolio and services).

### How do I automatically search ComeUp freelancers on comeup.com?

Ask an AI agent connected to Reduck to run reduck/comeup.com/search_freelancers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/comeup.com/search_freelancers

### Is there a comeup.com API to search ComeUp freelancers?

You do not need one. "Search ComeUp freelancers" drives the real comeup.com pages in a browser, so it works whether or not comeup.com offers an API for this.

### What information do I need to provide?

Required: query.

### What does it return?

It returns total, freelancers.

### Do I need to be logged in to comeup.com?

No. It only uses pages of comeup.com that are reachable without signing in.

### Does it change anything on comeup.com, or only read data?

It only reads. It looks things up on comeup.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/comeup.com/search_freelancers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/comeup.com/search_freelancers

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/comeup.com/search_freelancers
