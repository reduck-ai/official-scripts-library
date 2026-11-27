# Get an Auchan product

Automatically get an Auchan product on auchan.fr. Read one product of the Auchan France store (auchan.fr) from its product id, its reference or its link: name, brand, description, packaging, price in euros, price per kilo or per litre, availability, rating and review count, images, the breadcrumb of categories, and the offer the page shows first (offer id, seller id and type, delivery channel, stock), with the number of offers when marketplace sellers also sell it (Get Auchan product offers lists them). Auchan shows grocery prices only for a chosen store: pass a postcode and the script chooses the nearest drive or Click & Collect store the site lists for it, as a guest. Without a postcode, and when this browser has chosen no store before, grocery prices are null. An id or link that the store does not have fails with a message that says so.

- Site: auchan.fr
- Address: `reduck/auchan.fr/get-product`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/auchan.fr/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/auchan.fr/get-product
```

## Input

- `product` (string, required): The product id or reference from Search Auchan products (for example "C1178046"), or an auchan.fr product link.
- `postcode` (string, optional): French postcode (5 digits). When given, the script chooses the nearest drive or Click & Collect store Auchan lists for it, and the price is that store's.

## Output

- `url` (string, required)
- `name` (string | null, required)
- `productId` (string, required)
- `reference` (string | null, required)
- `brand` (string | null, optional)
- `price` (number | null, optional): Price in euros of the offer shown, null when the site shows none (no store chosen).
- `stock` (integer | null, optional)
- `store` (object | null, optional): The store this run chose from the postcode, or null when no postcode was given.
- `images` (array, optional)
- `rating` (number | null, optional)
- `seller` (string | null, optional): Marketplace seller of the offer shown; null for an offer of the Auchan store.
- `offerId` (string | null, optional)
- `currency` (string | null, optional)
- `sellerId` (string | null, optional)
- `packaging` (string | null, optional)
- `breadcrumb` (array, optional)
- `offerCount` (integer, optional): Number of sellers that offer the product (1 when only one offer is shown).
- `sellerType` (string | null, optional)
- `description` (string | null, optional)
- `reviewCount` (integer | null, optional)
- `availability` (string | null, optional): Availability as the page states it (a schema.org value).
- `canAddToCart` (boolean, optional)
- `pricePerUnit` (string | null, optional)
- `deliveryChannel` (string | null, optional)

## FAQ

### What does "Get an Auchan product" do?

Read one product of the Auchan France store (auchan.fr) from its product id, its reference or its link: name, brand, description, packaging, price in euros, price per kilo or per litre, availability, rating and review count, images, the breadcrumb of categories, and the offer the page shows first (offer id, seller id and type, delivery channel, stock), with the number of offers when marketplace sellers also sell it (Get Auchan product offers lists them). Auchan shows grocery prices only for a chosen store: pass a postcode and the script chooses the nearest drive or Click & Collect store the site lists for it, as a guest. Without a postcode, and when this browser has chosen no store before, grocery prices are null. An id or link that the store does not have fails with a message that says so.

### How do I automatically get an Auchan product on auchan.fr?

Ask an AI agent connected to Reduck to run reduck/auchan.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/auchan.fr/get-product

### Is there a auchan.fr API to get an Auchan product?

You do not need one. "Get an Auchan product" drives the real auchan.fr pages in a browser, so it works whether or not auchan.fr offers an API for this.

### What information do I need to provide?

Required: product. Optional: postcode.

### What does it return?

It returns url, name, brand, price, stock, store, images, rating, seller, offerId, currency, sellerId, packaging, productId, reference, breadcrumb, offerCount, sellerType, description, reviewCount, availability, canAddToCart, pricePerUnit, deliveryChannel.

### Do I need to be logged in to auchan.fr?

No. It only uses pages of auchan.fr that are reachable without signing in.

### Does it change anything on auchan.fr, or only read data?

It only reads. It looks things up on auchan.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/auchan.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/auchan.fr/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/auchan.fr/get-product
