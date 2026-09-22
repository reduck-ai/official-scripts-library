# Get Trending

Automatically get Trending on github.com. List GitHub's Trending repositories, a page with no official API, optionally filtered by language and period (daily/weekly/monthly). Returns repo, url, description, language, stars, forks, and stars gained over the period.

- Site: github.com
- Address: `reduck/github.com/get_trending`
- Updated: 2026-08-19 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/github.com/get_trending`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/github.com/get_trending
```

## Input

- `period` (string, optional): Date range (default daily)
- `language` (string, optional): Programming language filter, as typed on the page (e.g. "python", "typescript", "c++"). Omit for all languages.

## Output

- `count` (number, required)
- `repos` (array, required)
- `period` (string, required)
- `language` (string | null, optional)

## FAQ

### What does "Get Trending" do?

List GitHub's Trending repositories, a page with no official API, optionally filtered by language and period (daily/weekly/monthly). Returns repo, url, description, language, stars, forks, and stars gained over the period.

### How do I automatically get Trending on github.com?

Ask an AI agent connected to Reduck to run reduck/github.com/get_trending, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/github.com/get_trending

### Is there a github.com API to get Trending?

You do not need one. "Get Trending" drives the real github.com pages in a browser, so it works whether or not github.com offers an API for this.

### What information do I need to provide?

Optional: period, language.

### What does it return?

It returns count, repos, period, language.

### Do I need to be logged in to github.com?

No. It only uses pages of github.com that are reachable without signing in.

### Does it change anything on github.com, or only read data?

It only reads. It looks things up on github.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/github.com/get_trending, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/github.com/get_trending

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/github.com/get_trending
