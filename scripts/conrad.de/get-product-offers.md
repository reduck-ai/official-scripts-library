# Get Conrad product offers

Automatically get Conrad product offers on conrad.de. Get every offer the product page of Conrad Germany (conrad.de, the German store) lists for one product, from its Conrad product id (Bestell-Nr.) or product page link: for each offer the offer id, seller id and name (Conrad or a marketplace seller), price and currency in euros, whether the price includes VAT, condition, availability, stock, promised delivery date, minimum shipping cost and minimum order quantity, plus the offer id in the buy box. A browser with no account sees the business customer store, so prices are net prices without VAT. Pass an offer id to Add a product to the Conrad cart to choose the seller. An id that is not a Conrad product fails with an error that says so.

- Site: conrad.de
- Address: `reduck/conrad.de/get-product-offers`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/conrad.de/get-product-offers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/conrad.de/get-product-offers
```

## Input

- `product` (string, required): A Conrad product id (Bestell-Nr.) as Search Conrad products returns it, for example 3164696, or a conrad.de product page link.

## Output

- `url` (string, required)
- `name` (string | null, required)
- `offers` (array, required)
- `productId` (string, required)
- `buyBoxOfferId` (string | null, required): The offer the product page puts in its buy box.

## FAQ

### What does "Get Conrad product offers" do?

Get every offer the product page of Conrad Germany (conrad.de, the German store) lists for one product, from its Conrad product id (Bestell-Nr.) or product page link: for each offer the offer id, seller id and name (Conrad or a marketplace seller), price and currency in euros, whether the price includes VAT, condition, availability, stock, promised delivery date, minimum shipping cost and minimum order quantity, plus the offer id in the buy box. A browser with no account sees the business customer store, so prices are net prices without VAT. Pass an offer id to Add a product to the Conrad cart to choose the seller. An id that is not a Conrad product fails with an error that says so.

### How do I automatically get Conrad product offers on conrad.de?

Ask an AI agent connected to Reduck to run reduck/conrad.de/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/conrad.de/get-product-offers

### Is there a conrad.de API to get Conrad product offers?

You do not need one. "Get Conrad product offers" drives the real conrad.de pages in a browser, so it works whether or not conrad.de offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns url, name, offers, productId, buyBoxOfferId.

### Do I need to be logged in to conrad.de?

No. It only uses pages of conrad.de that are reachable without signing in.

### Does it change anything on conrad.de, or only read data?

It only reads. It looks things up on conrad.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/conrad.de/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/conrad.de/get-product-offers

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/conrad.de/get-product-offers
