# Get emag.ro product

Automatically get emag.ro product on emag.ro. Fetch one emag.ro product page by its product code or link (as Search emag products returns). Returns title, brand, barcode or manufacturer number, category path, price in lei (RON) and the recommended retail price when shown, stock status and whether it can be ordered, the seller of the offer shown with its rating, the product rating and review count, how many offers exist, the main image, the description and the technical attributes. An unknown product fails with an error that says so.

- Site: emag.ro
- Address: `reduck/emag.ro/get-product`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/emag.ro/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/emag.ro/get-product
```

## Input

- `product` (string, required): Link of an emag.ro product page or its product code, 9 capital letters and digits, as Search emag products gives it (pnk), for example DM9NN8MBM.

## Output

- `pnk` (string, required)
- `url` (string, required)
- `title` (string | null, required)
- `offerId` (string | null, required)
- `productId` (string, required)
- `mpn` (string | null, optional): Barcode or manufacturer number as the page gives it.
- `brand` (string | null, optional)
- `price` (number | null, optional)
- `rating` (number | null, optional)
- `seller` (string | null, optional)
- `category` (string | null, optional)
- `currency` (string | null, optional)
- `image_url` (string | null, optional)
- `orderable` (boolean | null, optional)
- `seller_id` (string | null, optional)
- `attributes` (array, optional)
- `breadcrumb` (array, optional)
- `list_price` (number | null, optional): Recommended retail price in lei when the page shows it.
- `description` (string | null, optional)
- `availability` (string | null, optional): Stock status code as the site marks it, for example in_stock.
- `offers_count` (integer | null, optional)
- `review_count` (integer | null, optional)
- `seller_rating` (number | null, optional)

## FAQ

### What does "Get emag.ro product" do?

Fetch one emag.ro product page by its product code or link (as Search emag products returns). Returns title, brand, barcode or manufacturer number, category path, price in lei (RON) and the recommended retail price when shown, stock status and whether it can be ordered, the seller of the offer shown with its rating, the product rating and review count, how many offers exist, the main image, the description and the technical attributes. An unknown product fails with an error that says so.

### How do I automatically get emag.ro product on emag.ro?

Ask an AI agent connected to Reduck to run reduck/emag.ro/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/emag.ro/get-product

### Is there a emag.ro API to get emag.ro product?

You do not need one. "Get emag.ro product" drives the real emag.ro pages in a browser, so it works whether or not emag.ro offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns mpn, pnk, url, brand, price, title, rating, seller, offerId, category, currency, image_url, orderable, productId, seller_id, attributes, breadcrumb, list_price, description, availability, offers_count, review_count, seller_rating.

### Do I need to be logged in to emag.ro?

No. It only uses pages of emag.ro that are reachable without signing in.

### Does it change anything on emag.ro, or only read data?

It only reads. It looks things up on emag.ro and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/emag.ro/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/emag.ro/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/emag.ro/get-product
