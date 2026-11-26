# Get Gifi product

Automatically get Gifi product on gifi.fr. Fetch one Gifi.fr product page from its product id (e.g. 577264) or its link (the url that Search Gifi products returns), both passed as url: id, name, price in euros, availability and condition as the site declares them, rating and review count, images, breadcrumb, whether the add button is enabled and the stock label shown. Gifi availability depends on the store chosen in the browser, so a product can read as unavailable until a store is selected. A page that does not exist fails with an error that says so; a link that is not a Gifi product page fails with an error.

- Site: gifi.fr
- Address: `reduck/gifi.fr/get-product`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/gifi.fr/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/gifi.fr/get-product
```

## Input

- `url` (string, required): Product page link on gifi.fr, as returned by Search Gifi products.

## Output

- `url` (string, required)
- `images` (array, required)
- `breadcrumb` (array, required)
- `add_to_cart_enabled` (boolean, required)
- `id` (string | null, optional)
- `name` (string | null, optional)
- `price` (number | null, optional)
- `rating` (number | null, optional)
- `currency` (string | null, optional)
- `condition` (string | null, optional)
- `availability` (string | null, optional)
- `review_count` (integer | null, optional)
- `in_store_stock_label` (string | null, optional)

## FAQ

### What does "Get Gifi product" do?

Fetch one Gifi.fr product page from its product id (e.g. 577264) or its link (the url that Search Gifi products returns), both passed as url: id, name, price in euros, availability and condition as the site declares them, rating and review count, images, breadcrumb, whether the add button is enabled and the stock label shown. Gifi availability depends on the store chosen in the browser, so a product can read as unavailable until a store is selected. A page that does not exist fails with an error that says so; a link that is not a Gifi product page fails with an error.

### How do I automatically get Gifi product on gifi.fr?

Ask an AI agent connected to Reduck to run reduck/gifi.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gifi.fr/get-product

### Is there a gifi.fr API to get Gifi product?

You do not need one. "Get Gifi product" drives the real gifi.fr pages in a browser, so it works whether or not gifi.fr offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns id, url, name, price, images, rating, currency, condition, breadcrumb, availability, review_count, add_to_cart_enabled, in_store_stock_label.

### Do I need to be logged in to gifi.fr?

No. It only uses pages of gifi.fr that are reachable without signing in.

### Does it change anything on gifi.fr, or only read data?

It only reads. It looks things up on gifi.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/gifi.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gifi.fr/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/gifi.fr/get-product
