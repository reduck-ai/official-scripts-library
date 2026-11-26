# Get ManoMano product

Automatically get ManoMano product on manomano.fr. Fetch one ManoMano.fr product page from its link (as returned by Search ManoMano products). Returns the product id, article id, title, brand, price and struck-through price in euros, discount, whether it can be bought, the seller of this offer with its country and the number of other sellers, minimum quantity, EAN, manufacturer reference, description, the technical attributes, images and the category breadcrumb. A link that is not a ManoMano product page fails with an error that says so.

- Site: manomano.fr
- Address: `reduck/manomano.fr/get-product`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/manomano.fr/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/manomano.fr/get-product
```

## Input

- `url` (string, required): Link of a ManoMano product page, as returned by Search ManoMano products, for example https://www.manomano.fr/p/vis-charpente-...-86361787?product_id=148926815.

## Output

- `url` (string, required)
- `title` (string | null, required)
- `articleId` (string | null, required)
- `productId` (string, required): The offer's product id, the one the cart uses.
- `ean` (string | null, optional)
- `brand` (string | null, optional)
- `price` (number | null, optional): Price in euros, taxes included.
- `images` (array, optional)
- `seller` (object | null, optional)
- `offerId` (string | null, optional)
- `currency` (string | null, optional)
- `available` (boolean | null, optional)
- `attributes` (array, optional)
- `breadcrumb` (array, optional)
- `list_price` (number | null, optional)
- `description` (string | null, optional)
- `second_hand` (boolean | null, optional)
- `discount_percent` (number | null, optional)
- `manufacturer_sku` (string | null, optional)
- `minimum_quantity` (integer | null, optional)
- `price_without_vat` (number | null, optional)
- `other_sellers_count` (integer | null, optional)

## FAQ

### What does "Get ManoMano product" do?

Fetch one ManoMano.fr product page from its link (as returned by Search ManoMano products). Returns the product id, article id, title, brand, price and struck-through price in euros, discount, whether it can be bought, the seller of this offer with its country and the number of other sellers, minimum quantity, EAN, manufacturer reference, description, the technical attributes, images and the category breadcrumb. A link that is not a ManoMano product page fails with an error that says so.

### How do I automatically get ManoMano product on manomano.fr?

Ask an AI agent connected to Reduck to run reduck/manomano.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/manomano.fr/get-product

### Is there a manomano.fr API to get ManoMano product?

You do not need one. "Get ManoMano product" drives the real manomano.fr pages in a browser, so it works whether or not manomano.fr offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns ean, url, brand, price, title, images, seller, offerId, currency, articleId, available, productId, attributes, breadcrumb, list_price, description, second_hand, discount_percent, manufacturer_sku, minimum_quantity, price_without_vat, other_sellers_count.

### Do I need to be logged in to manomano.fr?

No. It only uses pages of manomano.fr that are reachable without signing in.

### Does it change anything on manomano.fr, or only read data?

It only reads. It looks things up on manomano.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/manomano.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/manomano.fr/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/manomano.fr/get-product
