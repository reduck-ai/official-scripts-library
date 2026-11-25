# Get Darty product

Automatically get Darty product on darty.com. Fetch one Darty.com product page by its id (the product code that Search Darty products returns, for example 8194050). Returns title, brand, barcode number, price and struck-through list_price in euros, rating, review_count, availability, condition, seller, the number of sellers, shipping price, category, breadcrumb, images, description and the technical characteristics. An unknown id fails with an error that says so.

- Site: darty.com
- Address: `reduck/darty.com/get-product`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/darty.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/darty.com/get-product
```

## Input

- `id` (string, required): Darty product code as Search Darty products returns it: digits for a Darty product (for example 8194050), MC and digits for a marketplace product (for example MC351136810).

## Output

- `id` (string, required)
- `url` (string, required)
- `price` (number | null, required): Price in euros.
- `title` (string | null, required)
- `images` (array, required)
- `rating` (number | null, required): Average stars out of 5, null when there are no reviews.
- `attributes` (array, required): Technical characteristics, in page order. Several values of one characteristic are joined with commas.
- `breadcrumb` (array, required)
- `list_price` (number | null, required): Struck-through reference price in euros, null when none is shown.
- `availability` (string | null, required): schema.org availability the page declares, for example InStock or OutOfStock.
- `requested_id` (string, required)
- `review_count` (integer | null, required)
- `ean` (string | null, optional)
- `brand` (string | null, optional)
- `seller` (string | null, optional): Seller of the offer shown, DARTY for Darty itself.
- `category` (string | null, optional)
- `condition` (string | null, optional): Condition as Darty names it, for example neuf.
- `image_url` (string | null, optional)
- `description` (string | null, optional)
- `seller_count` (integer | null, optional): Number of sellers that offer this product.
- `shipping_price` (number | null, optional): Shipping price in euros that Darty states for the offer shown.

## FAQ

### What does "Get Darty product" do?

Fetch one Darty.com product page by its id (the product code that Search Darty products returns, for example 8194050). Returns title, brand, barcode number, price and struck-through list_price in euros, rating, review_count, availability, condition, seller, the number of sellers, shipping price, category, breadcrumb, images, description and the technical characteristics. An unknown id fails with an error that says so.

### How do I automatically get Darty product on darty.com?

Ask an AI agent connected to Reduck to run reduck/darty.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/darty.com/get-product

### Is there a darty.com API to get Darty product?

You do not need one. "Get Darty product" drives the real darty.com pages in a browser, so it works whether or not darty.com offers an API for this.

### What information do I need to provide?

Required: id.

### What does it return?

It returns id, ean, url, brand, price, title, images, rating, seller, category, condition, image_url, attributes, breadcrumb, list_price, description, availability, requested_id, review_count, seller_count, shipping_price.

### Do I need to be logged in to darty.com?

No. It only uses pages of darty.com that are reachable without signing in.

### Does it change anything on darty.com, or only read data?

It only reads. It looks things up on darty.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/darty.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/darty.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/darty.com/get-product
