# Get Boulanger product

Automatically get Boulanger product on boulanger.com. Fetch one Boulanger.com product page by its id (the product reference that Search Boulanger products returns, for example 1204873). Returns title, brand, barcode number, price and struck-through list_price in euros, rating, review_count, availability, condition, seller, breadcrumb, images, description and the technical characteristics. An unknown id fails with an error that says so.

- Site: boulanger.com
- Address: `reduck/boulanger.com/get-product`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/boulanger.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/boulanger.com/get-product
```

## Input

- `id` (string, required): Boulanger product reference as Search Boulanger products returns it, for example 1204873 (the number in a product URL after /ref/).

## Output

- `id` (string, required)
- `url` (string, required)
- `price` (number | null, required): Price in euros.
- `title` (string | null, required)
- `images` (array, required)
- `rating` (number | null, required): Average stars out of 5, null when there are no reviews.
- `attributes` (array, required): Technical characteristics, in page order.
- `breadcrumb` (array, required)
- `list_price` (number | null, required): Struck-through reference price in euros, null when none is shown.
- `availability` (string | null, required): schema.org availability the page declares, for example InStock or OutOfStock.
- `requested_id` (string, required)
- `review_count` (integer | null, required)
- `ean` (string | null, optional)
- `brand` (string | null, optional)
- `seller` (string | null, optional): boulanger, or the marketplace seller.
- `offer_id` (string | null, optional)
- `condition` (string | null, optional): Condition as Boulanger names it, for example neuf.
- `image_url` (string | null, optional)
- `description` (string | null, optional)

## FAQ

### What does "Get Boulanger product" do?

Fetch one Boulanger.com product page by its id (the product reference that Search Boulanger products returns, for example 1204873). Returns title, brand, barcode number, price and struck-through list_price in euros, rating, review_count, availability, condition, seller, breadcrumb, images, description and the technical characteristics. An unknown id fails with an error that says so.

### How do I automatically get Boulanger product on boulanger.com?

Ask an AI agent connected to Reduck to run reduck/boulanger.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/boulanger.com/get-product

### Is there a boulanger.com API to get Boulanger product?

You do not need one. "Get Boulanger product" drives the real boulanger.com pages in a browser, so it works whether or not boulanger.com offers an API for this.

### What information do I need to provide?

Required: id.

### What does it return?

It returns id, ean, url, brand, price, title, images, rating, seller, offer_id, condition, image_url, attributes, breadcrumb, list_price, description, availability, requested_id, review_count.

### Do I need to be logged in to boulanger.com?

No. It only uses pages of boulanger.com that are reachable without signing in.

### Does it change anything on boulanger.com, or only read data?

It only reads. It looks things up on boulanger.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/boulanger.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/boulanger.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/boulanger.com/get-product
