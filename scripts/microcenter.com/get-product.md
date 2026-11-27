# Get a Micro Center product

Automatically get a Micro Center product on microcenter.com. Get one Micro Center (microcenter.com) product by its link or product id, at one store: name, brand, SKU, manufacturer part number, price, currency, availability and the stock or shipping text the store shows, rating and review count when the page gives them, category path and images, plus the store the prices are for. Prices and stock depend on the store: pass store_id (three digits from the site's store picker, for example 081 for Fairfax, VA) or omit it for the web store 029 (shippable items) that Micro Center sets for a new guest. An unknown product id or a link that Micro Center answers with another page fails with an error that says so.

- Site: microcenter.com
- Address: `reduck/microcenter.com/get-product`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/microcenter.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/microcenter.com/get-product
```

## Input

- `url` (string, optional): Micro Center product link (https://www.microcenter.com/product/<id>/<name>), as Search Micro Center products returns it.
- `store_id` (string, optional): Micro Center store whose price and stock to show, three digits from the site's store picker, for example 081 (Fairfax, VA). Omit for the web store 029 (shippable items).
- `product_id` (string, optional): Micro Center product id (product_id of Search Micro Center products). Used when no url is given.

## Output

- `url` (string, required)
- `name` (string | null, required)
- `product_id` (string, required)
- `mpn` (string | null, optional): Manufacturer part number.
- `sku` (string | null, optional): Micro Center SKU number.
- `brand` (string | null, optional)
- `price` (number | null, optional): Price in US dollars at the store.
- `images` (array, optional)
- `rating` (number | null, optional)
- `currency` (string, optional)
- `store_id` (string | null, optional): The store whose price and stock are shown.
- `categories` (array, optional)
- `store_name` (string | null, optional)
- `availability` (string | null, optional): Availability as the page data gives it, for example InStock or OutOfStock.
- `review_count` (integer | null, optional)
- `availability_text` (string | null, optional): Stock or shipping text the store shows, for example "25+ NEW IN STOCK at Fairfax Store".

## FAQ

### What does "Get a Micro Center product" do?

Get one Micro Center (microcenter.com) product by its link or product id, at one store: name, brand, SKU, manufacturer part number, price, currency, availability and the stock or shipping text the store shows, rating and review count when the page gives them, category path and images, plus the store the prices are for. Prices and stock depend on the store: pass store_id (three digits from the site's store picker, for example 081 for Fairfax, VA) or omit it for the web store 029 (shippable items) that Micro Center sets for a new guest. An unknown product id or a link that Micro Center answers with another page fails with an error that says so.

### How do I automatically get a Micro Center product on microcenter.com?

Ask an AI agent connected to Reduck to run reduck/microcenter.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/microcenter.com/get-product

### Is there a microcenter.com API to get a Micro Center product?

You do not need one. "Get a Micro Center product" drives the real microcenter.com pages in a browser, so it works whether or not microcenter.com offers an API for this.

### What information do I need to provide?

Optional: url, store_id, product_id.

### What does it return?

It returns mpn, sku, url, name, brand, price, images, rating, currency, store_id, categories, product_id, store_name, availability, review_count, availability_text.

### Do I need to be logged in to microcenter.com?

No. It only uses pages of microcenter.com that are reachable without signing in.

### Does it change anything on microcenter.com, or only read data?

It only reads. It looks things up on microcenter.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/microcenter.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/microcenter.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/microcenter.com/get-product
