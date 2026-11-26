# Get Brico Depot product

Automatically get Brico Depot product on bricodepot.fr. Fetch one Brico Depot product (bricodepot.fr) by its sku (the id that Search Brico Depot products returns, for example 5063022538369) or by its product page link. Returns name, link, barcode, brand, price in euros (taxes included), struck-through price, price without tax, price per measure unit when the site gives one, unit, stock status, images, categories from the root down, and the characteristics the page shows (code and values). Prices and stock depend on the depot: without a depot id the site's default prices are returned and stock quantity is null; pass a depot id from Search Brico Depot depots to get that depot's price and stock. A link that is not a Brico Depot product page fails with an error, and so does a sku the site does not know.

- Site: bricodepot.fr
- Address: `reduck/bricodepot.fr/get-product`
- Updated: 2026-11-25 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bricodepot.fr/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bricodepot.fr/get-product
```

## Input

- `product` (string, required): Sku from Search Brico Depot products (for example 5063022538369), or a product page link such as https://www.bricodepot.fr/p/5063022538369/ruban-adhesif-d-emballage-66-m-marron.
- `depot_id` (integer, optional): Depot whose price and stock to show, the depot_id returned by Search Brico Depot depots. Without it the site's default prices apply and stock is not reported.

## Output

- `ean` (string | null, required)
- `sku` (string, required)
- `url` (string | null, required)
- `name` (string, required)
- `unit` (string | null, required)
- `brand` (string | null, required)
- `price` (number | null, required): Price in euros, taxes included.
- `images` (array, required)
- `rating` (number | null, required): Average customer rating out of 5; null when the product has no review.
- `currency` (string, required)
- `depot_id` (integer | null, required)
- `attributes` (array, required)
- `categories` (array, required)
- `list_price` (number | null, required): Struck-through regular price when the product is discounted.
- `description` (string | null, required): Product description of the page, as plain text with list items on their own lines. Null when the site has none.
- `review_count` (integer, required): Number of customer reviews.
- `stock_status` (string | null, required)
- `measure_price` (object | null, required)
- `price_excl_tax` (number | null, required)
- `stock_quantity` (integer | null, required): Units in the depot; null when no depot was given.
- `available_at_depot` (boolean | null, required): Whether the depot offers it for order; null when no depot was given.

## FAQ

### What does "Get Brico Depot product" do?

Fetch one Brico Depot product (bricodepot.fr) by its sku (the id that Search Brico Depot products returns, for example 5063022538369) or by its product page link. Returns name, link, barcode, brand, price in euros (taxes included), struck-through price, price without tax, price per measure unit when the site gives one, unit, stock status, images, categories from the root down, and the characteristics the page shows (code and values). Prices and stock depend on the depot: without a depot id the site's default prices are returned and stock quantity is null; pass a depot id from Search Brico Depot depots to get that depot's price and stock. A link that is not a Brico Depot product page fails with an error, and so does a sku the site does not know.

### How do I automatically get Brico Depot product on bricodepot.fr?

Ask an AI agent connected to Reduck to run reduck/bricodepot.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bricodepot.fr/get-product

### Is there a bricodepot.fr API to get Brico Depot product?

You do not need one. "Get Brico Depot product" drives the real bricodepot.fr pages in a browser, so it works whether or not bricodepot.fr offers an API for this.

### What information do I need to provide?

Required: product. Optional: depot_id.

### What does it return?

It returns ean, sku, url, name, unit, brand, price, images, rating, currency, depot_id, attributes, categories, list_price, description, review_count, stock_status, measure_price, price_excl_tax, stock_quantity, available_at_depot.

### Do I need to be logged in to bricodepot.fr?

No. It only uses pages of bricodepot.fr that are reachable without signing in.

### Does it change anything on bricodepot.fr, or only read data?

It only reads. It looks things up on bricodepot.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bricodepot.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bricodepot.fr/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/bricodepot.fr/get-product
