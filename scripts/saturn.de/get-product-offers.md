# Get SATURN product offers from all sellers

Automatically get SATURN product offers from all sellers on saturn.de. Lists every offer for a SATURN Germany (saturn.de, the German store) product: the offer of SATURN itself and the offers of Marketplace sellers, new and refurbished, as the product page's list of other offers shows them. Each offer has its offer id, price and struck-through price in euros, condition (new or refurbished grade), seller name, id, rating and review count, shipping cost and earliest and latest delivery dates. Pass the product id or link. The featured offer of the product page is marked. Use offer_id with Add a product to the SATURN cart to add one seller's offer. A product that has no offer on sale, or an unknown product id, is refused with a clear message.

- Site: saturn.de
- Address: `reduck/saturn.de/get-product-offers`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/saturn.de/get-product-offers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/saturn.de/get-product-offers
```

## Input

- `product` (string, required): SATURN product id (the product_id of Search SATURN products, the number at the end of a product link), or the product link itself.

## Output

- `url` (string, required)
- `title` (string | null, required)
- `offers` (array, required): The SATURN offer first when SATURN sells the product, then the Marketplace offers in the site's order.
- `product_id` (string, required)
- `total_offers` (integer, required): Number of offers in the list.

## FAQ

### What does "Get SATURN product offers from all sellers" do?

Lists every offer for a SATURN Germany (saturn.de, the German store) product: the offer of SATURN itself and the offers of Marketplace sellers, new and refurbished, as the product page's list of other offers shows them. Each offer has its offer id, price and struck-through price in euros, condition (new or refurbished grade), seller name, id, rating and review count, shipping cost and earliest and latest delivery dates. Pass the product id or link. The featured offer of the product page is marked. Use offer_id with Add a product to the SATURN cart to add one seller's offer. A product that has no offer on sale, or an unknown product id, is refused with a clear message.

### How do I automatically get SATURN product offers from all sellers on saturn.de?

Ask an AI agent connected to Reduck to run reduck/saturn.de/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/saturn.de/get-product-offers

### Is there a saturn.de API to get SATURN product offers from all sellers?

You do not need one. "Get SATURN product offers from all sellers" drives the real saturn.de pages in a browser, so it works whether or not saturn.de offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns url, title, offers, product_id, total_offers.

### Do I need to be logged in to saturn.de?

No. It only uses pages of saturn.de that are reachable without signing in.

### Does it change anything on saturn.de, or only read data?

It only reads. It looks things up on saturn.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/saturn.de/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/saturn.de/get-product-offers

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/saturn.de/get-product-offers
