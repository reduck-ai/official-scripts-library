# Get an HP product

Automatically get an HP product on hp.com. Get one product of the HP US store (hp.com/us-en/shop) by its link or its HP part number: name, brand, price after instant savings, list price (MSRP), the savings text, currency, availability, product class (STO for a fixed model, CTO for a model you customize), GTIN, rating, review count, category path and images. An unknown part number or a link that HP answers with another page fails with an error that says so; find the product with Search HP products.

- Site: hp.com
- Address: `reduck/hp.com/get-product`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hp.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hp.com/get-product
```

## Input

- `url` (string, optional): HP US store product link (https://www.hp.com/us-en/shop/pdp/...), as Search HP products returns it.
- `product_id` (string, optional): HP part number, for example 7P8K6AV_1 (product_id of Search HP products). Used when no url is given.

## Output

- `url` (string, required)
- `name` (string | null, required)
- `product_id` (string, required): HP part number.
- `gtin` (string | null, optional)
- `brand` (string | null, optional)
- `price` (number | null, optional): Price in US dollars, after the instant savings HP shows.
- `images` (array, optional)
- `rating` (number | null, optional): Average customer rating out of 5.
- `currency` (string, optional)
- `catalog_id` (string | null, optional): HP's internal catalog entry id of the product.
- `categories` (array, optional): Category path of the product page.
- `list_price` (number | null, optional): HP's suggested retail price (MSRP) in US dollars.
- `availability` (string | null, optional): Availability as HP gives it, for example InStock or OutOfStock.
- `review_count` (integer | null, optional)
- `product_class` (string | null, optional): STO for a fixed model, CTO for a model you can customize.
- `savings_message` (string | null, optional): The savings text HP shows, for example "Save $250 instantly".

## FAQ

### What does "Get an HP product" do?

Get one product of the HP US store (hp.com/us-en/shop) by its link or its HP part number: name, brand, price after instant savings, list price (MSRP), the savings text, currency, availability, product class (STO for a fixed model, CTO for a model you customize), GTIN, rating, review count, category path and images. An unknown part number or a link that HP answers with another page fails with an error that says so; find the product with Search HP products.

### How do I automatically get an HP product on hp.com?

Ask an AI agent connected to Reduck to run reduck/hp.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hp.com/get-product

### Is there a hp.com API to get an HP product?

You do not need one. "Get an HP product" drives the real hp.com pages in a browser, so it works whether or not hp.com offers an API for this.

### What information do I need to provide?

Optional: url, product_id.

### What does it return?

It returns url, gtin, name, brand, price, images, rating, currency, catalog_id, categories, list_price, product_id, availability, review_count, product_class, savings_message.

### Do I need to be logged in to hp.com?

No. It only uses pages of hp.com that are reachable without signing in.

### Does it change anything on hp.com, or only read data?

It only reads. It looks things up on hp.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hp.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hp.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/hp.com/get-product
