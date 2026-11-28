# Get Holland & Barrett product

Automatically get Holland & Barrett product on hollandandbarrett.com. Get one product of Holland & Barrett UK (hollandandbarrett.com, the United Kingdom store) from its Holland & Barrett product id or product page link: sku, name, brand, link, category, description (as the site's HTML), images, price and earlier price in pounds (GBP), discount percent, price per unit, promotions, availability and stock status, whether a marketplace seller sells it, rating and review count, and the other sizes of the product (each a product of its own, with its id, label, price and availability). An id that is not a Holland & Barrett product fails with an error that says so.

- Site: hollandandbarrett.com
- Address: `reduck/hollandandbarrett.com/get-product`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hollandandbarrett.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hollandandbarrett.com/get-product
```

## Input

- `product` (string, required): A Holland & Barrett product id as Search Holland & Barrett products returns it, for example 6100005252, or a hollandandbarrett.com product page link.

## Output

- `url` (string | null, required)
- `name` (string | null, required)
- `brand` (string | null, required)
- `price` (number | null, required): Price in the currency given.
- `sizes` (array, required)
- `skuId` (string, required): The sku the basket uses for this product.
- `rating` (number | null, required): Average rating out of 5.
- `category` (string | null, required)
- `currency` (string | null, required)
- `wasPrice` (number | null, required)
- `imageUrls` (array, required)
- `productId` (string, required)
- `promotions` (array, required)
- `marketplace` (boolean | null, required)
- `reviewCount` (number | null, required)
- `stockStatus` (string | null, required): For example IN_STOCK.
- `availability` (string | null, required)
- `pricePerUnit` (string | null, required)
- `descriptionHtml` (string | null, required)
- `discountPercent` (number | null, required)

## FAQ

### What does "Get Holland & Barrett product" do?

Get one product of Holland & Barrett UK (hollandandbarrett.com, the United Kingdom store) from its Holland & Barrett product id or product page link: sku, name, brand, link, category, description (as the site's HTML), images, price and earlier price in pounds (GBP), discount percent, price per unit, promotions, availability and stock status, whether a marketplace seller sells it, rating and review count, and the other sizes of the product (each a product of its own, with its id, label, price and availability). An id that is not a Holland & Barrett product fails with an error that says so.

### How do I automatically get Holland & Barrett product on hollandandbarrett.com?

Ask an AI agent connected to Reduck to run reduck/hollandandbarrett.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hollandandbarrett.com/get-product

### Is there a hollandandbarrett.com API to get Holland & Barrett product?

You do not need one. "Get Holland & Barrett product" drives the real hollandandbarrett.com pages in a browser, so it works whether or not hollandandbarrett.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns url, name, brand, price, sizes, skuId, rating, category, currency, wasPrice, imageUrls, productId, promotions, marketplace, reviewCount, stockStatus, availability, pricePerUnit, descriptionHtml, discountPercent.

### Do I need to be logged in to hollandandbarrett.com?

No. It only uses pages of hollandandbarrett.com that are reachable without signing in.

### Does it change anything on hollandandbarrett.com, or only read data?

It only reads. It looks things up on hollandandbarrett.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hollandandbarrett.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hollandandbarrett.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/hollandandbarrett.com/get-product
