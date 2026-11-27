# Search Auchan products

Automatically search Auchan products on auchan.fr. Search the products of the Auchan France store (auchan.fr) by keyword, one results page at a time, in the order the site gives (sponsored products included and marked). For each product: its id and reference (to pass to Get an Auchan product or Add a product to the Auchan cart), name, brand, link, image, packaging, price in euros, price per kilo or per litre, review count, availability, seller (the store, or the marketplace seller), offer id, categories and promotion flags, plus the total number of results. Auchan shows grocery prices only for a chosen store: pass a postcode and the script chooses the nearest drive or Click & Collect store the site lists for it, as a guest. Without a postcode, and when this browser has chosen no store before, grocery prices are null and the site states why. A search with no exact match gives a null total and either an empty list or the loose suggestions the site lists; a page past the end returns an empty list.

- Site: auchan.fr
- Address: `reduck/auchan.fr/search-products`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/auchan.fr/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/auchan.fr/search-products
```

## Input

- `query` (string, required): Words to search for, as typed in the site's search box (for example "lait").
- `page` (integer, optional): Results page, from 1.
- `postcode` (string, optional): French postcode (5 digits). When given, the script chooses the nearest drive or Click & Collect store Auchan lists for it, and the prices are that store's.

## Output

- `url` (string, required)
- `page` (integer, required)
- `query` (string, required)
- `store` (object | null, required): The store this run chose from the postcode, or null when no postcode was given.
- `total` (integer | null, required): Number of results the site states for the search.
- `hasMore` (boolean, required): True when a next page has products.
- `products` (array, required)

## FAQ

### What does "Search Auchan products" do?

Search the products of the Auchan France store (auchan.fr) by keyword, one results page at a time, in the order the site gives (sponsored products included and marked). For each product: its id and reference (to pass to Get an Auchan product or Add a product to the Auchan cart), name, brand, link, image, packaging, price in euros, price per kilo or per litre, review count, availability, seller (the store, or the marketplace seller), offer id, categories and promotion flags, plus the total number of results. Auchan shows grocery prices only for a chosen store: pass a postcode and the script chooses the nearest drive or Click & Collect store the site lists for it, as a guest. Without a postcode, and when this browser has chosen no store before, grocery prices are null and the site states why. A search with no exact match gives a null total and either an empty list or the loose suggestions the site lists; a page past the end returns an empty list.

### How do I automatically search Auchan products on auchan.fr?

Ask an AI agent connected to Reduck to run reduck/auchan.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/auchan.fr/search-products

### Is there a auchan.fr API to search Auchan products?

You do not need one. "Search Auchan products" drives the real auchan.fr pages in a browser, so it works whether or not auchan.fr offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, postcode.

### What does it return?

It returns url, page, query, store, total, hasMore, products.

### Do I need to be logged in to auchan.fr?

No. It only uses pages of auchan.fr that are reachable without signing in.

### Does it change anything on auchan.fr, or only read data?

It only reads. It looks things up on auchan.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/auchan.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/auchan.fr/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/auchan.fr/search-products
