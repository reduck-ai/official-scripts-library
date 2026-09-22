# Search Leboncoin ads

Automatically search Leboncoin ads on leboncoin.fr. Search Leboncoin classifieds by keyword and/or location. Returns total, max_pages, count, and ads (each with id, url, title, price_eur, currency, city, zipcode, category_id, category_name, seller_type, published_at, thumb_url, image_count). Paging is capped at max_pages=100.

- Site: leboncoin.fr
- Address: `reduck/leboncoin.fr/search`
- Updated: 2026-09-17 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/leboncoin.fr/search`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/search
```

## Input

- `page` (integer, optional): Page index (capped at max_pages=100).
- `text` (string, optional): Free-text query, e.g. 'iphone 13' or 'table en chêne'. The aliases query, keyword and keywords are accepted for the same thing; pass whichever you have.
- `query` (string, optional): Alias for text. Accepted because it is a common name for a search term; it behaves identically.
- `keyword` (string, optional): Alias for text. Accepted because it is a common name for a search term; it behaves identically.
- `keywords` (string, optional): Alias for text. Accepted because it is a common name for a search term; it behaves identically.
- `locations` (any, optional): City name, a comma-separated list of cities, or an array of city names, e.g. 'Paris', 'Paris,Lyon' or ['Paris','Lyon']. An empty array counts as no location filter.

## Output

- `ads` (array, required)
- `count` (integer, required)
- `total` (integer, required)
- `max_pages` (integer, required)

## FAQ

### What does "Search Leboncoin ads" do?

Search Leboncoin classifieds by keyword and/or location. Returns total, max_pages, count, and ads (each with id, url, title, price_eur, currency, city, zipcode, category_id, category_name, seller_type, published_at, thumb_url, image_count). Paging is capped at max_pages=100.

### How do I automatically search Leboncoin ads on leboncoin.fr?

Ask an AI agent connected to Reduck to run reduck/leboncoin.fr/search, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/search

### Is there a leboncoin.fr API to search Leboncoin ads?

You do not need one. "Search Leboncoin ads" drives the real leboncoin.fr pages in a browser, so it works whether or not leboncoin.fr offers an API for this.

### What information do I need to provide?

Optional: page, text, query, keyword, keywords, locations.

### What does it return?

It returns ads, count, total, max_pages.

### Do I need to be logged in to leboncoin.fr?

No. It only uses pages of leboncoin.fr that are reachable without signing in.

### Does it change anything on leboncoin.fr, or only read data?

It only reads. It looks things up on leboncoin.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/leboncoin.fr/search, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/search

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/leboncoin.fr/search
