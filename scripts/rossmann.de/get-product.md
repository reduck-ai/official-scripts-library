# Get Rossmann product

Automatically get Rossmann product on rossmann.de. Read one product of the Rossmann Germany online shop (rossmann.de) from its barcode number or product page link: Rossmann article number, name, brand, pack size, price, struck-through earlier price and base price in euros, promotion label, badges, online stock status and quantity, delivery window, sales channel, order quantity limits, rating, review count, categories, images, the text sections of the page (description, use, ingredients and more) and the variants of the product. A barcode number or link that Rossmann does not know fails with a message that says so.

- Site: rossmann.de
- Address: `reduck/rossmann.de/get-product`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/rossmann.de/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/rossmann.de/get-product
```

## Input

- `product` (string, required): The product's barcode number (the productId of Search Rossmann products) or a rossmann.de product page link.

## Output

- `link` (string, required)
- `name` (string | null, required)
- `size` (string | null, required): Pack size as the site shows it, for example 400 ml.
- `brand` (string | null, required)
- `price` (number | null, required): Price in euros.
- `images` (array, required)
- `labels` (array, required): Badges the site shows on the product.
- `rating` (number | null, required): Average rating out of 5.
- `details` (array, required): Text sections of the page, in German, as the site gives them.
- `currency` (string, required)
- `variants` (array, required): Other variants of the product (for example shades), each with its own EAN.
- `listPrice` (number | null, required): Struck-through earlier price in euros, when the site shows one.
- `productId` (string, required): Barcode number (EAN).
- `unitPrice` (number | null, required): Base price in euros, per unitPriceBase.
- `categories` (array, required)
- `deliveryTo` (string | null, required): Latest delivery date (ISO 8601).
- `reviewCount` (integer | null, required)
- `availability` (string | null, required): Online stock status as the site gives it, for example inStock.
- `deliveryFrom` (string | null, required): Earliest delivery date (ISO 8601).
- `salesChannel` (string | null, required): Where the product is sold: ONLINE, STORE or BOTH, as the site gives it.
- `articleNumber` (string | null, required): Rossmann's own article number (DAN).
- `stockQuantity` (integer | null, required): Units in online stock, as the site gives it.
- `storeDelivery` (boolean | null, required): True when it can be delivered to a store.
- `unitPriceBase` (string | null, required): Quantity the base price is for, for example 1 L.
- `promotionLabel` (string | null, required)
- `maxOrderQuantity` (integer | null, required)
- `minOrderQuantity` (integer | null, required)
- `outOfStockMessage` (string | null, required)
- `listPriceIsRecommendedRetailPrice` (boolean, required)

## FAQ

### What does "Get Rossmann product" do?

Read one product of the Rossmann Germany online shop (rossmann.de) from its barcode number or product page link: Rossmann article number, name, brand, pack size, price, struck-through earlier price and base price in euros, promotion label, badges, online stock status and quantity, delivery window, sales channel, order quantity limits, rating, review count, categories, images, the text sections of the page (description, use, ingredients and more) and the variants of the product. A barcode number or link that Rossmann does not know fails with a message that says so.

### How do I automatically get Rossmann product on rossmann.de?

Ask an AI agent connected to Reduck to run reduck/rossmann.de/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/rossmann.de/get-product

### Is there a rossmann.de API to get Rossmann product?

You do not need one. "Get Rossmann product" drives the real rossmann.de pages in a browser, so it works whether or not rossmann.de offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns link, name, size, brand, price, images, labels, rating, details, currency, variants, listPrice, productId, unitPrice, categories, deliveryTo, reviewCount, availability, deliveryFrom, salesChannel, articleNumber, stockQuantity, storeDelivery, unitPriceBase, promotionLabel, maxOrderQuantity, minOrderQuantity, outOfStockMessage, listPriceIsRecommendedRetailPrice.

### Do I need to be logged in to rossmann.de?

No. It only uses pages of rossmann.de that are reachable without signing in.

### Does it change anything on rossmann.de, or only read data?

It only reads. It looks things up on rossmann.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/rossmann.de/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/rossmann.de/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/rossmann.de/get-product
