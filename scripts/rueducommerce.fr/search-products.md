# Search Rue du Commerce products

Automatically search Rue du Commerce products on rueducommerce.fr. Searches rueducommerce.fr for a free-text query and returns one page of results (up to 48 products) with price in euros, seller type, availability and the ids needed to read a product or add it to the cart. Returns an empty list when nothing matches. Use page to go further.

- Site: rueducommerce.fr
- Address: `reduck/rueducommerce.fr/search-products`
- Updated: 2026-11-24 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/rueducommerce.fr/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/rueducommerce.fr/search-products
```

## Input

- `query` (string, required): Free-text search, e.g. "clavier sans fil".
- `page` (integer, optional): Result page, starting at 1 (48 products per page).

## Output

- `page` (integer, required)
- `query` (string, required)
- `products` (array, required)
- `hasNextPage` (boolean, required)
- `totalResults` (integer | null, optional)

## FAQ

### What does "Search Rue du Commerce products" do?

Searches rueducommerce.fr for a free-text query and returns one page of results (up to 48 products) with price in euros, seller type, availability and the ids needed to read a product or add it to the cart. Returns an empty list when nothing matches. Use page to go further.

### How do I automatically search Rue du Commerce products on rueducommerce.fr?

Ask an AI agent connected to Reduck to run reduck/rueducommerce.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/rueducommerce.fr/search-products

### Is there a rueducommerce.fr API to search Rue du Commerce products?

You do not need one. "Search Rue du Commerce products" drives the real rueducommerce.fr pages in a browser, so it works whether or not rueducommerce.fr offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, query, products, hasNextPage, totalResults.

### Do I need to be logged in to rueducommerce.fr?

No. It only uses pages of rueducommerce.fr that are reachable without signing in.

### Does it change anything on rueducommerce.fr, or only read data?

It only reads. It looks things up on rueducommerce.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/rueducommerce.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/rueducommerce.fr/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/rueducommerce.fr/search-products
