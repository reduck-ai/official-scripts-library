# Search Tripadvisor

Automatically search Tripadvisor on tripadvisor.com. Search Tripadvisor's typeahead for places (restaurants, hotels, attractions, cities): name, location id, address, coordinates, and place type. No login required.

- Site: tripadvisor.com
- Address: `reduck/tripadvisor.com/search`
- Updated: 2026-09-02 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tripadvisor.com/search`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tripadvisor.com/search
```

## Input

- `query` (string, required): Search keywords, e.g. "sushi tokyo" or "Le Comptoir du Relais"

## Output

- `query` (string, required)
- `results` (array, required)

## FAQ

### What does "Search Tripadvisor" do?

Search Tripadvisor's typeahead for places (restaurants, hotels, attractions, cities): name, location id, address, coordinates, and place type. No login required.

### How do I automatically search Tripadvisor on tripadvisor.com?

Ask an AI agent connected to Reduck to run reduck/tripadvisor.com/search, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tripadvisor.com/search

### Is there a tripadvisor.com API to search Tripadvisor?

You do not need one. "Search Tripadvisor" drives the real tripadvisor.com pages in a browser, so it works whether or not tripadvisor.com offers an API for this.

### What information do I need to provide?

Required: query.

### What does it return?

It returns query, results.

### Do I need to be logged in to tripadvisor.com?

No. It only uses pages of tripadvisor.com that are reachable without signing in.

### Does it change anything on tripadvisor.com, or only read data?

It only reads. It looks things up on tripadvisor.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tripadvisor.com/search, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tripadvisor.com/search

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tripadvisor.com/search
