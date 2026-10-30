# Get Google AI Overview

Automatically get Google AI Overview on google.com. Run a Google search and return the AI Overview Google shows for it: whether there is one, its answer as Markdown (headings, lists, tables and links kept), and the pages it cites, in the order the answer first cites them, each with url, title, site, byline and snippet. Google shows an AI Overview for some searches only: for the others shown is false and sources is empty. The overview follows the browser's Google account, location and moment, so the same search can get a different overview, or none, on another run. When Google shows its anti-bot check and it cannot be cleared, the run fails and says so.

- Site: google.com
- Address: `reduck/google.com/get_ai_overview`
- Updated: 2026-10-29 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/google.com/get_ai_overview`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/google.com/get_ai_overview
```

## Input

- `query` (string, required): The search, as typed in Google, e.g. 'how to get reddit keyword alerts'.

## Output

- `text` (string | null, required): The overview's answer as Markdown. Each citation chip is kept in its place as links to the pages it stands for, e.g. "([MCP Servers](https://…), [reduck.ai](https://…))". Null when there is no overview.
- `shown` (boolean, required): True when Google shows an AI Overview for this search.
- `sources` (array, required): The pages the overview cites, one per page, in the order the answer first cites them. Empty when there is no overview.

## FAQ

### What does "Get Google AI Overview" do?

Run a Google search and return the AI Overview Google shows for it: whether there is one, its answer as Markdown (headings, lists, tables and links kept), and the pages it cites, in the order the answer first cites them, each with url, title, site, byline and snippet. Google shows an AI Overview for some searches only: for the others shown is false and sources is empty. The overview follows the browser's Google account, location and moment, so the same search can get a different overview, or none, on another run. When Google shows its anti-bot check and it cannot be cleared, the run fails and says so.

### How do I automatically get Google AI Overview on google.com?

Ask an AI agent connected to Reduck to run reduck/google.com/get_ai_overview, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/get_ai_overview

### Is there a google.com API to get Google AI Overview?

You do not need one. "Get Google AI Overview" drives the real google.com pages in a browser, so it works whether or not google.com offers an API for this.

### What information do I need to provide?

Required: query.

### What does it return?

It returns text, shown, sources.

### Do I need to be logged in to google.com?

No. It only uses pages of google.com that are reachable without signing in.

### Does it change anything on google.com, or only read data?

It only reads. It looks things up on google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/google.com/get_ai_overview, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/get_ai_overview

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/google.com/get_ai_overview
