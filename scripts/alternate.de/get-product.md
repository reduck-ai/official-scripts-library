# Get Alternate product

Automatically get Alternate product on alternate.de. Get one product of Alternate Germany (alternate.de, the German store) from its Alternate product id (Art.-Nr.) or product page link: name, brand, category, link, image, description, barcode number, manufacturer part number, price and currency (euros, VAT included), availability, condition, seller, average rating out of 5 and rating count, and whether the page offers an add to cart button. An id that is not an Alternate product fails with an error that says so.

- Site: alternate.de
- Address: `reduck/alternate.de/get-product`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/alternate.de/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/alternate.de/get-product
```

## Input

- `product` (string, required): An Alternate product id (Art.-Nr.) as Search Alternate products returns it, for example 1864243, or an alternate.de product page link.

## Output

- `ean` (string | null, required)
- `url` (string | null, required)
- `name` (string | null, required)
- `brand` (string | null, required)
- `price` (number | null, required): Price in the currency given, VAT included.
- `rating` (number | null, required): Average rating out of 5.
- `seller` (string | null, required)
- `category` (string | null, required)
- `currency` (string | null, required)
- `imageUrl` (string | null, required)
- `condition` (string | null, required): For example NewCondition.
- `productId` (string, required)
- `description` (string | null, required)
- `ratingCount` (number | null, required)
- `availability` (string | null, required): Availability as the site gives it to search engines, for example InStock.
- `canAddToCart` (boolean, required): True when the product page shows an add to cart button.
- `manufacturerPartNumber` (string | null, required)

## FAQ

### What does "Get Alternate product" do?

Get one product of Alternate Germany (alternate.de, the German store) from its Alternate product id (Art.-Nr.) or product page link: name, brand, category, link, image, description, barcode number, manufacturer part number, price and currency (euros, VAT included), availability, condition, seller, average rating out of 5 and rating count, and whether the page offers an add to cart button. An id that is not an Alternate product fails with an error that says so.

### How do I automatically get Alternate product on alternate.de?

Ask an AI agent connected to Reduck to run reduck/alternate.de/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/alternate.de/get-product

### Is there a alternate.de API to get Alternate product?

You do not need one. "Get Alternate product" drives the real alternate.de pages in a browser, so it works whether or not alternate.de offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns ean, url, name, brand, price, rating, seller, category, currency, imageUrl, condition, productId, description, ratingCount, availability, canAddToCart, manufacturerPartNumber.

### Do I need to be logged in to alternate.de?

No. It only uses pages of alternate.de that are reachable without signing in.

### Does it change anything on alternate.de, or only read data?

It only reads. It looks things up on alternate.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/alternate.de/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/alternate.de/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/alternate.de/get-product
