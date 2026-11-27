# Get Auchan product offers

Automatically get Auchan product offers on auchan.fr. List every offer for one product of the Auchan France store (auchan.fr): Auchan has a marketplace, so one product can be sold by several sellers. For each offer: the offer id and seller id (to pass to Add a product to the Auchan cart), the seller name, the seller type, the price and the price before discount in euros, the delivery channel, the delivery promise and its price as the site writes them, and whether it is the offer the site shows first. A product sold only by the Auchan store gives one offer, with the store's price when a store is chosen: pass a postcode and the script chooses the nearest drive or Click & Collect store the site lists for it, as a guest. A product id or link that the store does not have fails with a message that says so.

- Site: auchan.fr
- Address: `reduck/auchan.fr/get-product-offers`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/auchan.fr/get-product-offers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/auchan.fr/get-product-offers
```

## Input

- `product` (string, required): The product id or reference from Search Auchan products, or an auchan.fr product link.
- `postcode` (string, optional): French postcode (5 digits). When given, the script chooses the nearest drive or Click & Collect store Auchan lists for it.

## Output

- `url` (string, required)
- `name` (string | null, required)
- `offers` (array, required)
- `productId` (string, required)
- `store` (object | null, optional)

## FAQ

### What does "Get Auchan product offers" do?

List every offer for one product of the Auchan France store (auchan.fr): Auchan has a marketplace, so one product can be sold by several sellers. For each offer: the offer id and seller id (to pass to Add a product to the Auchan cart), the seller name, the seller type, the price and the price before discount in euros, the delivery channel, the delivery promise and its price as the site writes them, and whether it is the offer the site shows first. A product sold only by the Auchan store gives one offer, with the store's price when a store is chosen: pass a postcode and the script chooses the nearest drive or Click & Collect store the site lists for it, as a guest. A product id or link that the store does not have fails with a message that says so.

### How do I automatically get Auchan product offers on auchan.fr?

Ask an AI agent connected to Reduck to run reduck/auchan.fr/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/auchan.fr/get-product-offers

### Is there a auchan.fr API to get Auchan product offers?

You do not need one. "Get Auchan product offers" drives the real auchan.fr pages in a browser, so it works whether or not auchan.fr offers an API for this.

### What information do I need to provide?

Required: product. Optional: postcode.

### What does it return?

It returns url, name, store, offers, productId.

### Do I need to be logged in to auchan.fr?

No. It only uses pages of auchan.fr that are reachable without signing in.

### Does it change anything on auchan.fr, or only read data?

It only reads. It looks things up on auchan.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/auchan.fr/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/auchan.fr/get-product-offers

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/auchan.fr/get-product-offers
