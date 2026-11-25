# Get Argos product

Automatically get Argos product on argos.co.uk. Fetch one Argos (argos.co.uk) product page by product number or product link. Returns title, link, brand, barcode number, price and earlier price in pounds sterling, offer text, rating and review count, main image and all images, description with specifications as plain text, category path, delivery and store collection flags, out-of-stock flag, delivery cost, seller, and every version of the product (color, size) with its own product number and price. An unknown product number fails with an error that says so.

- Site: argos.co.uk
- Address: `reduck/argos.co.uk/get-product`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/argos.co.uk/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/argos.co.uk/get-product
```

## Input

- `product` (string, required): Argos product number (the product_id of Search Argos products, the number after /product/ in a link), or the product link itself.

## Output

- `url` (string, required)
- `price` (number | null, required): Price in pounds sterling (GBP), VAT included.
- `title` (string | null, required)
- `requested` (string, required)
- `product_id` (string, required)
- `ean` (string | null, optional): EAN barcode.
- `brand` (string | null, optional)
- `images` (array, optional)
- `rating` (number | null, optional): Average rating out of 5. Null when nobody rated the product.
- `seller` (string | null, optional): Argos, or the partner seller's name.
- `variants` (array, optional): Every version of the product (color, size), this one included, each with its own product number. Empty when there is one version.
- `image_url` (string | null, optional)
- `breadcrumb` (array, optional)
- `list_price` (number | null, optional): Earlier price in pounds shown struck through, null when none.
- `offer_text` (string | null, optional): The offer line, as Argos writes it, for example "Save £5.00".
- `collectable` (boolean | null, optional): It can be collected in a store.
- `deliverable` (boolean | null, optional): Argos can deliver it.
- `description` (string | null, optional): Description and specifications as plain text, list items starting with "- ".
- `out_of_stock` (boolean | null, optional): True when Argos shows it out of stock everywhere.
- `review_count` (integer | null, optional)
- `delivery_cost` (number | null, optional): Delivery cost in pounds.
- `free_delivery` (boolean | null, optional)

## FAQ

### What does "Get Argos product" do?

Fetch one Argos (argos.co.uk) product page by product number or product link. Returns title, link, brand, barcode number, price and earlier price in pounds sterling, offer text, rating and review count, main image and all images, description with specifications as plain text, category path, delivery and store collection flags, out-of-stock flag, delivery cost, seller, and every version of the product (color, size) with its own product number and price. An unknown product number fails with an error that says so.

### How do I automatically get Argos product on argos.co.uk?

Ask an AI agent connected to Reduck to run reduck/argos.co.uk/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/argos.co.uk/get-product

### Is there a argos.co.uk API to get Argos product?

You do not need one. "Get Argos product" drives the real argos.co.uk pages in a browser, so it works whether or not argos.co.uk offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns ean, url, brand, price, title, images, rating, seller, variants, image_url, requested, breadcrumb, list_price, offer_text, product_id, collectable, deliverable, description, out_of_stock, review_count, delivery_cost, free_delivery.

### Do I need to be logged in to argos.co.uk?

No. It only uses pages of argos.co.uk that are reachable without signing in.

### Does it change anything on argos.co.uk, or only read data?

It only reads. It looks things up on argos.co.uk and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/argos.co.uk/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/argos.co.uk/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/argos.co.uk/get-product
