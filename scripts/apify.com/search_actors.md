# Search Apify Store actors

Automatically search Apify Store actors on apify.com. Search the Apify Store (apify.com/store) for actors, the ready-made scrapers and automation APIs Apify sells, by keyword, developer and pricing model, sorted as the Store sorts. Returns one page of results with the total match count, and for each actor its id (owner/name, the input of apify.com/get_actor_pricing), title, description, developer, categories, rating, review count, user counts, Store URL and its pricing in effect now (model and every chargeable event with its price in USD per Apify plan tier). Prices are per single event; the Store shows them per 1,000. Page with offset. A search with no match returns an empty list. Anonymous, read-only.

- Site: apify.com
- Address: `reduck/apify.com/search_actors`
- Updated: 2026-11-16 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/apify.com/search_actors`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/apify.com/search_actors
```

## Input

- `limit` (integer, optional): How many actors to return.
- `query` (string, optional): Keywords to search for, e.g. "google maps". Omit to list the whole Store.
- `offset` (integer, optional): How many matching actors to skip, for paging.
- `sortBy` (string, optional): The Store's sort order.
- `developer` (string, optional): Only actors of this developer, by username (the owner part of an actor id, e.g. compass).
- `pricingModel` (string, optional): Only actors with this pricing model.

## Output

- `total` (integer, required): How many actors match in all.
- `actors` (array, required)
- `offset` (integer, required)

## FAQ

### What does "Search Apify Store actors" do?

Search the Apify Store (apify.com/store) for actors, the ready-made scrapers and automation APIs Apify sells, by keyword, developer and pricing model, sorted as the Store sorts. Returns one page of results with the total match count, and for each actor its id (owner/name, the input of apify.com/get_actor_pricing), title, description, developer, categories, rating, review count, user counts, Store URL and its pricing in effect now (model and every chargeable event with its price in USD per Apify plan tier). Prices are per single event; the Store shows them per 1,000. Page with offset. A search with no match returns an empty list. Anonymous, read-only.

### How do I automatically search Apify Store actors on apify.com?

Ask an AI agent connected to Reduck to run reduck/apify.com/search_actors, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/apify.com/search_actors

### Is there a apify.com API to search Apify Store actors?

You do not need one. "Search Apify Store actors" drives the real apify.com pages in a browser, so it works whether or not apify.com offers an API for this.

### What information do I need to provide?

Optional: limit, query, offset, sortBy, developer, pricingModel.

### What does it return?

It returns total, actors, offset.

### Do I need to be logged in to apify.com?

No. It only uses pages of apify.com that are reachable without signing in.

### Does it change anything on apify.com, or only read data?

It only reads. It looks things up on apify.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/apify.com/search_actors, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/apify.com/search_actors

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/apify.com/search_actors
