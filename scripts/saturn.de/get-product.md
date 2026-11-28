# Get SATURN product

Automatically get SATURN product on saturn.de. Fetch one SATURN Germany (saturn.de, the German store) product page by product id or product link. Returns title, link, brand, barcode number, price and struck-through price of the featured offer in euros, discount, rating and review count, main image and all images, delivery status and dates, shipping cost, seller (SATURN or a Marketplace seller) with the Marketplace offer id, category path, description, technical data and the other versions of the product (colors, sizes) with their ids. For the offers of other sellers, use Get SATURN product offers. Texts are in German. An unknown product id fails with an error that says so.

- Site: saturn.de
- Address: `reduck/saturn.de/get-product`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/saturn.de/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/saturn.de/get-product
```

## Input

- `product` (string, required): SATURN product id (the product_id of Search SATURN products, the number at the end of a product link), or the product link itself.

## Output

- `url` (string | null, required)
- `price` (number | null, required): Price of the featured offer as shown, VAT included, in the currency of currency.
- `title` (string | null, required)
- `seller` (string | null, required): SATURN, or the name of the Marketplace seller of the featured offer.
- `currency` (string | null, required): Currency of the prices, EUR.
- `requested` (string, required): The product argument as given.
- `product_id` (string, required): SATURN product id.
- `ean` (string | null, optional): EAN (GTIN-13) barcode.
- `brand` (string | null, optional)
- `images` (array, optional)
- `rating` (number | null, optional): Average rating out of 5. Null when nobody rated the product.
- `offer_id` (string | null, optional): Id of the featured Marketplace offer. Null when SATURN sells the product.
- `variants` (array, optional): Other versions of the product (color, size), each its own product id. Empty when there are none.
- `image_url` (string | null, optional)
- `seller_id` (string | null, optional): Marketplace seller id, null when SATURN sells it.
- `breadcrumb` (array, optional): Category path, in German. Empty when the page shows none.
- `list_price` (number | null, optional): Struck-through comparison price, null when none is shown.
- `description` (string | null, optional): Product description as plain text.
- `marketplace` (boolean | null, optional): True when a Marketplace seller sells the featured offer, not SATURN.
- `availability` (string | null, optional): Delivery status as SATURN codes it, for example AVAILABLE or NOT_AVAILABLE.
- `review_count` (integer | null, optional)
- `shipping_cost` (number | null, optional): Shipping cost in euros.
- `specifications` (array, optional): Technical data as the site lists it, in German.
- `delivery_latest` (string | null, optional): Latest delivery, ISO 8601.
- `list_price_type` (string | null, optional): What list_price is, as SATURN names it, for example RRP (manufacturer's recommended price) or LOP (lowest price of the last 30 days).
- `delivery_earliest` (string | null, optional): Earliest delivery, ISO 8601.
- `discount_percentage` (number | null, optional)

## FAQ

### What does "Get SATURN product" do?

Fetch one SATURN Germany (saturn.de, the German store) product page by product id or product link. Returns title, link, brand, barcode number, price and struck-through price of the featured offer in euros, discount, rating and review count, main image and all images, delivery status and dates, shipping cost, seller (SATURN or a Marketplace seller) with the Marketplace offer id, category path, description, technical data and the other versions of the product (colors, sizes) with their ids. For the offers of other sellers, use Get SATURN product offers. Texts are in German. An unknown product id fails with an error that says so.

### How do I automatically get SATURN product on saturn.de?

Ask an AI agent connected to Reduck to run reduck/saturn.de/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/saturn.de/get-product

### Is there a saturn.de API to get SATURN product?

You do not need one. "Get SATURN product" drives the real saturn.de pages in a browser, so it works whether or not saturn.de offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns ean, url, brand, price, title, images, rating, seller, currency, offer_id, variants, image_url, requested, seller_id, breadcrumb, list_price, product_id, description, marketplace, availability, review_count, shipping_cost, specifications, delivery_latest, list_price_type, delivery_earliest, discount_percentage.

### Do I need to be logged in to saturn.de?

No. It only uses pages of saturn.de that are reachable without signing in.

### Does it change anything on saturn.de, or only read data?

It only reads. It looks things up on saturn.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/saturn.de/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/saturn.de/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/saturn.de/get-product
