# Search Alza.cz products

Automatically search Alza.cz products on alza.cz. Search Alza.cz (Czech shop, prices in Czech crowns) for products by free text and return one page of results: each product with its id, code, name, link, price and whether it can be bought. Pass a page number to go further; the result says whether a next page exists. A search the site sends to a single category returns that category's products.

- Site: alza.cz
- Address: `reduck/alza.cz/search-products`
- Updated: 2026-11-24 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/alza.cz/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/alza.cz/search-products
```

## Input

- `query` (string, required): Free text to search, for example baterie aa.
- `page` (integer, optional): Result page, starting at 1.

## Output

- `page` (integer, required)
- `query` (string, required)
- `pageUrl` (string, required): Address of the result page the site showed.
- `products` (array, required)
- `hasNextPage` (boolean, required)

## FAQ

### What does "Search Alza.cz products" do?

Search Alza.cz (Czech shop, prices in Czech crowns) for products by free text and return one page of results: each product with its id, code, name, link, price and whether it can be bought. Pass a page number to go further; the result says whether a next page exists. A search the site sends to a single category returns that category's products.

### How do I automatically search Alza.cz products on alza.cz?

Ask an AI agent connected to Reduck to run reduck/alza.cz/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/alza.cz/search-products

### Is there a alza.cz API to search Alza.cz products?

You do not need one. "Search Alza.cz products" drives the real alza.cz pages in a browser, so it works whether or not alza.cz offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, query, pageUrl, products, hasNextPage.

### Do I need to be logged in to alza.cz?

No. It only uses pages of alza.cz that are reachable without signing in.

### Does it change anything on alza.cz, or only read data?

It only reads. It looks things up on alza.cz and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/alza.cz/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/alza.cz/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/alza.cz/search-products
