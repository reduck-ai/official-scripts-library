# Get Currys product

Automatically get Currys product on currys.co.uk. Fetch one Currys (currys.co.uk) product page by product number or product link. Returns title, link, brand, barcode number, price and price before the reduction in pounds sterling, rating and review count, stock, delivery and store collection availability, main image and all images, description, category path, delivery options with their cost, technical specifications, and every version of the product (color, size) with its own product number and price. An unknown product number fails with an error that says so.

- Site: currys.co.uk
- Address: `reduck/currys.co.uk/get-product`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/currys.co.uk/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/currys.co.uk/get-product
```

## Input

- `product` (string, required): Currys product number (the product_id of Search Currys products, the number at the end of a product link), or the product link itself.

## Output

- `url` (string, required)
- `price` (number | null, required): Price in pounds sterling (GBP), VAT included.
- `title` (string | null, required)
- `requested` (string, required)
- `product_id` (string, required)
- `ean` (string | null, optional)
- `brand` (string | null, optional)
- `images` (array, optional)
- `rating` (number | null, optional): Average rating out of 5. Null when nobody rated the product.
- `shipping` (array, optional): Delivery options the page declares, with their cost.
- `variants` (array, optional): Every version of the product (color, size), this one included. Empty when there is one version.
- `image_url` (string | null, optional)
- `breadcrumb` (array, optional)
- `list_price` (number | null, optional): Price in pounds before the current reduction, null when there is none.
- `description` (string | null, optional)
- `availability` (string | null, optional): Stock as the page declares it, for example InStock or OutOfStock.
- `review_count` (integer | null, optional)
- `specifications` (array, optional)
- `delivery_available` (boolean | null, optional)
- `collection_available` (boolean | null, optional): It can be collected in a store.

## FAQ

### What does "Get Currys product" do?

Fetch one Currys (currys.co.uk) product page by product number or product link. Returns title, link, brand, barcode number, price and price before the reduction in pounds sterling, rating and review count, stock, delivery and store collection availability, main image and all images, description, category path, delivery options with their cost, technical specifications, and every version of the product (color, size) with its own product number and price. An unknown product number fails with an error that says so.

### How do I automatically get Currys product on currys.co.uk?

Ask an AI agent connected to Reduck to run reduck/currys.co.uk/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/currys.co.uk/get-product

### Is there a currys.co.uk API to get Currys product?

You do not need one. "Get Currys product" drives the real currys.co.uk pages in a browser, so it works whether or not currys.co.uk offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns ean, url, brand, price, title, images, rating, shipping, variants, image_url, requested, breadcrumb, list_price, product_id, description, availability, review_count, specifications, delivery_available, collection_available.

### Do I need to be logged in to currys.co.uk?

No. It only uses pages of currys.co.uk that are reachable without signing in.

### Does it change anything on currys.co.uk, or only read data?

It only reads. It looks things up on currys.co.uk and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/currys.co.uk/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/currys.co.uk/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/currys.co.uk/get-product
