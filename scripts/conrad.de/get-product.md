# Get Conrad product

Automatically get Conrad product on conrad.de. Get one product of Conrad Germany (conrad.de, the German store) from its Conrad product id (Bestell-Nr.) or product page link: name, canonical link, brand, manufacturer part number, barcode number, category, whether it can be bought, images, review count, technical details, the offer in the buy box (offer id, seller, price and currency in euros, whether the price includes VAT, condition, availability, stock, delivery date, minimum shipping cost, minimum order quantity) and how many offers there are. A browser with no account sees the business customer store, so prices are net prices without VAT. Use Get Conrad product offers for every seller's offer. An id that is not a Conrad product fails with an error that says so.

- Site: conrad.de
- Address: `reduck/conrad.de/get-product`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/conrad.de/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/conrad.de/get-product
```

## Input

- `product` (string, required): A Conrad product id (Bestell-Nr.) as Search Conrad products returns it, for example 3164696, or a conrad.de product page link.

## Output

- `ean` (string | null, required)
- `url` (string, required): The product page link.
- `name` (string | null, required)
- `brand` (string | null, required)
- `offer` (any, required): The offer in the buy box, or null when no seller offers the product.
- `buyable` (boolean | null, required)
- `category` (string | null, required)
- `imageUrls` (array, required)
- `productId` (string, required)
- `offerCount` (integer, required): How many offers the product page lists.
- `reviewCount` (integer | null, required)
- `technicalDetails` (array, required)
- `manufacturerPartNumber` (string | null, required)

## FAQ

### What does "Get Conrad product" do?

Get one product of Conrad Germany (conrad.de, the German store) from its Conrad product id (Bestell-Nr.) or product page link: name, canonical link, brand, manufacturer part number, barcode number, category, whether it can be bought, images, review count, technical details, the offer in the buy box (offer id, seller, price and currency in euros, whether the price includes VAT, condition, availability, stock, delivery date, minimum shipping cost, minimum order quantity) and how many offers there are. A browser with no account sees the business customer store, so prices are net prices without VAT. Use Get Conrad product offers for every seller's offer. An id that is not a Conrad product fails with an error that says so.

### How do I automatically get Conrad product on conrad.de?

Ask an AI agent connected to Reduck to run reduck/conrad.de/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/conrad.de/get-product

### Is there a conrad.de API to get Conrad product?

You do not need one. "Get Conrad product" drives the real conrad.de pages in a browser, so it works whether or not conrad.de offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns ean, url, name, brand, offer, buyable, category, imageUrls, productId, offerCount, reviewCount, technicalDetails, manufacturerPartNumber.

### Do I need to be logged in to conrad.de?

No. It only uses pages of conrad.de that are reachable without signing in.

### Does it change anything on conrad.de, or only read data?

It only reads. It looks things up on conrad.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/conrad.de/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/conrad.de/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/conrad.de/get-product
