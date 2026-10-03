# Search Kleinanzeigen listings

Automatically search Kleinanzeigen listings on kleinanzeigen.de. Search Kleinanzeigen (Germany's largest classifieds marketplace) by keyword across Germany, one results page at a time. Returns each listing's id, link, title, short description, price as shown and as a number, location, posting date, whether it can be bought directly, and image, plus the total number of matching listings.

- Site: kleinanzeigen.de
- Address: `reduck/kleinanzeigen.de/search_listings`
- Updated: 2026-10-02 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/kleinanzeigen.de/search_listings`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/kleinanzeigen.de/search_listings
```

## Input

- `query` (string, required): What to search for, e.g. "fahrrad", "iphone 15", "sofa".
- `page` (integer, optional): Results page, 1-based (25 listings per page).

## Output

- `page` (integer, required)
- `query` (string, required)
- `total` (integer | null, required): Number of matching listings across Germany, as the site reports it.
- `listings` (array, required): Listings in page order, including promoted ones. Empty when nothing matches.

## FAQ

### What does "Search Kleinanzeigen listings" do?

Search Kleinanzeigen (Germany's largest classifieds marketplace) by keyword across Germany, one results page at a time. Returns each listing's id, link, title, short description, price as shown and as a number, location, posting date, whether it can be bought directly, and image, plus the total number of matching listings.

### How do I automatically search Kleinanzeigen listings on kleinanzeigen.de?

Ask an AI agent connected to Reduck to run reduck/kleinanzeigen.de/search_listings, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kleinanzeigen.de/search_listings

### Is there a kleinanzeigen.de API to search Kleinanzeigen listings?

You do not need one. "Search Kleinanzeigen listings" drives the real kleinanzeigen.de pages in a browser, so it works whether or not kleinanzeigen.de offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, query, total, listings.

### Do I need to be logged in to kleinanzeigen.de?

No. It only uses pages of kleinanzeigen.de that are reachable without signing in.

### Does it change anything on kleinanzeigen.de, or only read data?

It only reads. It looks things up on kleinanzeigen.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/kleinanzeigen.de/search_listings, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kleinanzeigen.de/search_listings

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/kleinanzeigen.de/search_listings
