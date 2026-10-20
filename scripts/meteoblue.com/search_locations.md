# Search meteoblue locations

Automatically search meteoblue locations on meteoblue.com. Search meteoblue's location index by place name, as its search box does, and get one page of matching places in meteoblue's order: name, region, country, coordinates, timezone, id and the location url that meteoblue.com/get_14day_forecast takes. Pass page to read further pages; an unknown name returns an empty list.

- Site: meteoblue.com
- Address: `reduck/meteoblue.com/search_locations`
- Updated: 2026-10-19 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/meteoblue.com/search_locations`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/meteoblue.com/search_locations
```

## Input

- `query` (string, required): Place name, e.g. "Paris" or "Marina di Andora".
- `page` (integer, optional): Result page, 10 places per page.

## Output

- `page` (integer, required)
- `query` (string, required)
- `locations` (array, required)
- `pages` (integer | null, optional): How many pages meteoblue has for this query.

## FAQ

### What does "Search meteoblue locations" do?

Search meteoblue's location index by place name, as its search box does, and get one page of matching places in meteoblue's order: name, region, country, coordinates, timezone, id and the location url that meteoblue.com/get_14day_forecast takes. Pass page to read further pages; an unknown name returns an empty list.

### How do I automatically search meteoblue locations on meteoblue.com?

Ask an AI agent connected to Reduck to run reduck/meteoblue.com/search_locations, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/meteoblue.com/search_locations

### Is there a meteoblue.com API to search meteoblue locations?

You do not need one. "Search meteoblue locations" drives the real meteoblue.com pages in a browser, so it works whether or not meteoblue.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, pages, query, locations.

### Do I need to be logged in to meteoblue.com?

No. It only uses pages of meteoblue.com that are reachable without signing in.

### Does it change anything on meteoblue.com, or only read data?

It only reads. It looks things up on meteoblue.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/meteoblue.com/search_locations, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/meteoblue.com/search_locations

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/meteoblue.com/search_locations
