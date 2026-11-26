# Get LDLC product

Automatically get LDLC product on ldlc.com. Fetch one LDLC.com product page by its product id (for example PB00630480, as Search LDLC products returns it) or its page link. Returns the name, brand, barcode number, manufacturer reference, price and struck-through list price in euros, availability and condition as the page declares them, the seller, rating and review count, the images, the short description, the category breadcrumb and the technical specifications as name and value pairs. An unknown product fails with an error that says so.

- Site: ldlc.com
- Address: `reduck/ldlc.com/get-product`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ldlc.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ldlc.com/get-product
```

## Input

- `product` (string, required): Product id (PB00630480) or product page link (https://www.ldlc.com/fiche/PB00630480.html), from Search LDLC products.

## Output

- `mpn` (string | null, required): Manufacturer reference.
- `url` (string, required)
- `gtin` (string | null, required): Barcode number.
- `name` (string | null, required)
- `brand` (string | null, required)
- `price` (number | null, required): Price in euros, taxes included.
- `specs` (array, required)
- `images` (array, required)
- `rating` (number | null, required)
- `seller` (string | null, required)
- `offerId` (string | null, required): Id of the offer the page shows, the one the cart holds.
- `currency` (string | null, required)
- `condition` (string | null, required): For example NewCondition.
- `productId` (string, required)
- `breadcrumb` (array, required)
- `list_price` (number | null, required)
- `description` (string | null, required)
- `availability` (string | null, required): As the page declares it, for example InStock or OutOfStock.
- `review_count` (integer | null, required)
- `price_valid_until` (string | null, required)

## FAQ

### What does "Get LDLC product" do?

Fetch one LDLC.com product page by its product id (for example PB00630480, as Search LDLC products returns it) or its page link. Returns the name, brand, barcode number, manufacturer reference, price and struck-through list price in euros, availability and condition as the page declares them, the seller, rating and review count, the images, the short description, the category breadcrumb and the technical specifications as name and value pairs. An unknown product fails with an error that says so.

### How do I automatically get LDLC product on ldlc.com?

Ask an AI agent connected to Reduck to run reduck/ldlc.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ldlc.com/get-product

### Is there a ldlc.com API to get LDLC product?

You do not need one. "Get LDLC product" drives the real ldlc.com pages in a browser, so it works whether or not ldlc.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns mpn, url, gtin, name, brand, price, specs, images, rating, seller, offerId, currency, condition, productId, breadcrumb, list_price, description, availability, review_count, price_valid_until.

### Do I need to be logged in to ldlc.com?

No. It only uses pages of ldlc.com that are reachable without signing in.

### Does it change anything on ldlc.com, or only read data?

It only reads. It looks things up on ldlc.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ldlc.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ldlc.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/ldlc.com/get-product
