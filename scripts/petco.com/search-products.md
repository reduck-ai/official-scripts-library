# Search Petco products

Automatically search Petco products on petco.com. Search Petco (petco.com, US) products by keywords, 48 a page, in the order of the site. For each product: id, name, link, brand, rating, review count, lowest and highest price and the price before the sale in US dollars, image, and each size or flavor with its item number, name, link and price. Also gives the total count and the number of pages. A page past the last one gives an empty list. For keywords that match no product, Petco shows the products it finds closest. Use a managed browser in the US.

- Site: petco.com
- Address: `reduck/petco.com/search-products`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/petco.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/petco.com/search-products
```

## Input

- `query` (string, required): Keywords, for example "dog food".
- `page` (integer, optional): Results page, 48 products a page.

## Output

- `page` (integer, required)
- `pages` (integer, required): Number of result pages.
- `query` (string, required)
- `total` (integer, required): Number of products that match, on all pages.
- `products` (array, required)

## FAQ

### What does "Search Petco products" do?

Search Petco (petco.com, US) products by keywords, 48 a page, in the order of the site. For each product: id, name, link, brand, rating, review count, lowest and highest price and the price before the sale in US dollars, image, and each size or flavor with its item number, name, link and price. Also gives the total count and the number of pages. A page past the last one gives an empty list. For keywords that match no product, Petco shows the products it finds closest. Use a managed browser in the US.

### How do I automatically search Petco products on petco.com?

Ask an AI agent connected to Reduck to run reduck/petco.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/petco.com/search-products

### Is there a petco.com API to search Petco products?

You do not need one. "Search Petco products" drives the real petco.com pages in a browser, so it works whether or not petco.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, pages, query, total, products.

### Do I need to be logged in to petco.com?

No. It only uses pages of petco.com that are reachable without signing in.

### Does it change anything on petco.com, or only read data?

It only reads. It looks things up on petco.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/petco.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/petco.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/petco.com/search-products
