# Get MediaMarkt Spain product

Automatically get MediaMarkt Spain product on mediamarkt.es. Fetch one MediaMarkt Spain (mediamarkt.es) product page by product id or product link. Returns title, link, brand, barcode number, price and struck-through price in euros, discount, rating and review count, main image and all images, delivery status and dates, shipping cost, seller (MediaMarkt or a Marketplace seller), category path, description, technical data, the other versions of the product (colors, sizes) with their ids, and every offer the page holds (new and refurbished, each with price, condition and seller). Texts are in Spanish. An unknown product id fails with an error that says so.

- Site: mediamarkt.es
- Address: `reduck/mediamarkt.es/get-product`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mediamarkt.es/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mediamarkt.es/get-product
```

## Input

- `product` (string, required): MediaMarkt Spain product id (the product_id of Search MediaMarkt Spain products, the number at the end of a product link), or the product link itself.

## Output

- `url` (string | null, required)
- `price` (number | null, required): Price in euros as shown, VAT included.
- `title` (string | null, required)
- `offers` (array, required): Every offer of the product the page holds: new and refurbished, from MediaMarkt or Marketplace sellers. Empty when the page lists only the main offer.
- `seller` (string | null, required): MediaMarkt, or the name of the Marketplace seller.
- `requested` (string, required): The product argument as given.
- `product_id` (string, required): MediaMarkt product id.
- `ean` (string | null, optional): EAN (GTIN-13) barcode.
- `brand` (string | null, optional)
- `images` (array, optional)
- `rating` (number | null, optional): Average rating out of 5. Null when nobody rated the product.
- `variants` (array, optional): Other versions of the product (color, size), each its own product id. Empty when there are none.
- `image_url` (string | null, optional)
- `seller_id` (string | null, optional): Marketplace seller id, null when MediaMarkt sells it.
- `breadcrumb` (array, optional): Category path, in Spanish.
- `list_price` (number | null, optional): Struck-through comparison price in euros, null when none is shown.
- `description` (string | null, optional): Product description as plain text.
- `marketplace` (boolean | null, optional): True when a Marketplace seller sells the product, not MediaMarkt.
- `availability` (string | null, optional): Delivery status as MediaMarkt codes it, for example AVAILABLE, PARTIALLY_AVAILABLE or NOT_AVAILABLE.
- `review_count` (integer | null, optional)
- `shipping_cost` (number | null, optional): Shipping cost in euros.
- `specifications` (array, optional): Technical data as the site lists it, in Spanish.
- `delivery_latest` (string | null, optional): Latest delivery, ISO 8601.
- `list_price_type` (string | null, optional): What list_price is, as MediaMarkt names it: RRP (manufacturer's recommended price) or LOP (lowest price of the last 30 days).
- `delivery_earliest` (string | null, optional): Earliest delivery, ISO 8601.
- `discount_percentage` (number | null, optional)

## FAQ

### What does "Get MediaMarkt Spain product" do?

Fetch one MediaMarkt Spain (mediamarkt.es) product page by product id or product link. Returns title, link, brand, barcode number, price and struck-through price in euros, discount, rating and review count, main image and all images, delivery status and dates, shipping cost, seller (MediaMarkt or a Marketplace seller), category path, description, technical data, the other versions of the product (colors, sizes) with their ids, and every offer the page holds (new and refurbished, each with price, condition and seller). Texts are in Spanish. An unknown product id fails with an error that says so.

### How do I automatically get MediaMarkt Spain product on mediamarkt.es?

Ask an AI agent connected to Reduck to run reduck/mediamarkt.es/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mediamarkt.es/get-product

### Is there a mediamarkt.es API to get MediaMarkt Spain product?

You do not need one. "Get MediaMarkt Spain product" drives the real mediamarkt.es pages in a browser, so it works whether or not mediamarkt.es offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns ean, url, brand, price, title, images, offers, rating, seller, variants, image_url, requested, seller_id, breadcrumb, list_price, product_id, description, marketplace, availability, review_count, shipping_cost, specifications, delivery_latest, list_price_type, delivery_earliest, discount_percentage.

### Do I need to be logged in to mediamarkt.es?

No. It only uses pages of mediamarkt.es that are reachable without signing in.

### Does it change anything on mediamarkt.es, or only read data?

It only reads. It looks things up on mediamarkt.es and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mediamarkt.es/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mediamarkt.es/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/mediamarkt.es/get-product
