# Search Conrad products

Automatically search Conrad products on conrad.de. Search products on Conrad Germany (conrad.de, the German store) by keywords, and get one page of results in the order the site gives for relevance: each product with its Conrad product id, name, link, brand, manufacturer part number, barcode number, image, price and currency (euros), whether the price includes VAT, the offer id and seller of the offer shown, how many other offers there are, availability, and placement (result, sponsored or highlighted). A browser with no account sees the business customer store, so prices are net prices without VAT. A page has up to 90 results: pass page for the next ones. A search with no match, or a page after the last result, gives an empty list. Some words (a brand or a category) send the site to a category page instead: then the list is empty and redirectUrl gives that page.

- Site: conrad.de
- Address: `reduck/conrad.de/search-products`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/conrad.de/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/conrad.de/search-products
```

## Input

- `query` (string, required): Search words, a product id or a manufacturer part number, as typed in the Conrad search box.
- `page` (integer, optional): The result page, from 1. Conrad shows up to 90 results on a page.

## Output

- `from` (integer | null, required): The position of the first result of this page, from 0.
- `page` (integer, required)
- `query` (string, required)
- `total` (integer | null, required): The number of results Conrad gives for the search.
- `pageSize` (integer | null, required): The number of results Conrad asked for on this page.
- `products` (array, required)
- `redirectUrl` (string | null, required): When Conrad sends this search to a category or brand page instead of results, the link of that page. Then products is empty.
- `totalIsExact` (boolean | null, required): False when Conrad gives the total as a lower bound (it stops counting at 2000).
- `correctedQuery` (string | null, required): The words Conrad searched instead, when it corrected the query.

## FAQ

### What does "Search Conrad products" do?

Search products on Conrad Germany (conrad.de, the German store) by keywords, and get one page of results in the order the site gives for relevance: each product with its Conrad product id, name, link, brand, manufacturer part number, barcode number, image, price and currency (euros), whether the price includes VAT, the offer id and seller of the offer shown, how many other offers there are, availability, and placement (result, sponsored or highlighted). A browser with no account sees the business customer store, so prices are net prices without VAT. A page has up to 90 results: pass page for the next ones. A search with no match, or a page after the last result, gives an empty list. Some words (a brand or a category) send the site to a category page instead: then the list is empty and redirectUrl gives that page.

### How do I automatically search Conrad products on conrad.de?

Ask an AI agent connected to Reduck to run reduck/conrad.de/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/conrad.de/search-products

### Is there a conrad.de API to search Conrad products?

You do not need one. "Search Conrad products" drives the real conrad.de pages in a browser, so it works whether or not conrad.de offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns from, page, query, total, pageSize, products, redirectUrl, totalIsExact, correctedQuery.

### Do I need to be logged in to conrad.de?

No. It only uses pages of conrad.de that are reachable without signing in.

### Does it change anything on conrad.de, or only read data?

It only reads. It looks things up on conrad.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/conrad.de/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/conrad.de/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/conrad.de/search-products
