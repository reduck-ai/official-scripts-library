# Search Agencies (Clutch)

Automatically search Agencies (Clutch) on clutch.co. Lists agencies from Clutch's public agency directory for a given service category, with rating, price range, size, location, and a short description of each firm.

- Site: clutch.co
- Address: `reduck/clutch.co/search_agencies`
- Updated: 2026-09-18 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/clutch.co/search_agencies`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/clutch.co/search_agencies
```

## Input

- `category` (string, required): Clutch's category URL slug, e.g. "digital-marketing", "web-development", "it-services", "mobile-app-development" (matches the segment after clutch.co/agencies/ on the category's own page).
- `page` (integer, optional): 1-based page of results, matching Clutch's own pagination.

## Output

- `page` (integer, required)
- `found` (boolean, required)
- `agencies` (array, required)
- `category` (string, required)

## FAQ

### What does "Search Agencies (Clutch)" do?

Lists agencies from Clutch's public agency directory for a given service category, with rating, price range, size, location, and a short description of each firm.

### How do I automatically search Agencies (Clutch) on clutch.co?

Ask an AI agent connected to Reduck to run reduck/clutch.co/search_agencies, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/clutch.co/search_agencies

### Is there a clutch.co API to search Agencies (Clutch)?

You do not need one. "Search Agencies (Clutch)" drives the real clutch.co pages in a browser, so it works whether or not clutch.co offers an API for this.

### What information do I need to provide?

Required: category. Optional: page.

### What does it return?

It returns page, found, agencies, category.

### Do I need to be logged in to clutch.co?

No. It only uses pages of clutch.co that are reachable without signing in.

### Does it change anything on clutch.co, or only read data?

It only reads. It looks things up on clutch.co and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/clutch.co/search_agencies, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/clutch.co/search_agencies

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/clutch.co/search_agencies
