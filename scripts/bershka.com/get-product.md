# Get Bershka product

Automatically get Bershka product on bershka.com. Get one product of the Bershka France store (bershka.com/fr) from its product id or its link: name, description, reference, and every colour with its price and old price in euros, link, and every size once for each length it comes in (short, regular, long), with its offerId (the id that Add Bershka product to cart takes), price and stock state. A product id that Bershka does not know gives an error that tells you to search again.

- Site: bershka.com
- Address: `reduck/bershka.com/get-product`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bershka.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bershka.com/get-product
```

## Input

- `product` (string, required): Product id (such as the productId of Search Bershka products) or the link of a Bershka product page.

## Output

- `url` (string, required)
- `name` (string | null, required)
- `colors` (array, required): Every colour of the product, each with every size.
- `currency` (string, required): Currency of the prices, as an ISO code (euro).
- `productId` (string, required)
- `description` (string | null, required)
- `displayReference` (string | null, required): Reference the page shows.

## FAQ

### What does "Get Bershka product" do?

Get one product of the Bershka France store (bershka.com/fr) from its product id or its link: name, description, reference, and every colour with its price and old price in euros, link, and every size once for each length it comes in (short, regular, long), with its offerId (the id that Add Bershka product to cart takes), price and stock state. A product id that Bershka does not know gives an error that tells you to search again.

### How do I automatically get Bershka product on bershka.com?

Ask an AI agent connected to Reduck to run reduck/bershka.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bershka.com/get-product

### Is there a bershka.com API to get Bershka product?

You do not need one. "Get Bershka product" drives the real bershka.com pages in a browser, so it works whether or not bershka.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns url, name, colors, currency, productId, description, displayReference.

### Do I need to be logged in to bershka.com?

No. It only uses pages of bershka.com that are reachable without signing in.

### Does it change anything on bershka.com, or only read data?

It only reads. It looks things up on bershka.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bershka.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bershka.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/bershka.com/get-product
