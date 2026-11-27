# Search Mercado Livre products

Automatically search Mercado Livre products on mercadolibre.com. Search Mercado Livre Brazil (mercadolivre.com.br) products by keyword, one results page (about 50) at a time. Returns each result's listing id, catalog id, name, clean product link, price, list price, seller, official-store and sponsored flags, plus the total count; a search with no match or a page past the last returns an empty list.

- Site: mercadolibre.com
- Address: `reduck/mercadolibre.com/search-products`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mercadolibre.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mercadolibre.com/search-products
```

## Input

- `query` (string, required): Keywords, e.g. 'fone bluetooth'.
- `page` (integer, optional): Results page, about 50 results each.

## Output

- `page` (integer, required)
- `query` (string, required)
- `total` (integer | null, required): Result count as Mercado Livre states it.
- `products` (array, required)

## FAQ

### What does "Search Mercado Livre products" do?

Search Mercado Livre Brazil (mercadolivre.com.br) products by keyword, one results page (about 50) at a time. Returns each result's listing id, catalog id, name, clean product link, price, list price, seller, official-store and sponsored flags, plus the total count; a search with no match or a page past the last returns an empty list.

### How do I automatically search Mercado Livre products on mercadolibre.com?

Ask an AI agent connected to Reduck to run reduck/mercadolibre.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mercadolibre.com/search-products

### Is there a mercadolibre.com API to search Mercado Livre products?

You do not need one. "Search Mercado Livre products" drives the real mercadolibre.com pages in a browser, so it works whether or not mercadolibre.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, query, total, products.

### Do I need to be logged in to mercadolibre.com?

Yes. It acts as you on mercadolibre.com: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for mercadolibre.com.

### Does it change anything on mercadolibre.com, or only read data?

It only reads. It looks things up on mercadolibre.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mercadolibre.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mercadolibre.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/mercadolibre.com/search-products
