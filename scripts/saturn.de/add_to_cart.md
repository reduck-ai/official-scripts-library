# Add a product to the SATURN cart

Automatically add a product to the SATURN cart on saturn.de. Add a product to the guest shopping cart of this browser on SATURN Germany (saturn.de, the German store), by product id or product link, with a quantity from 1 to 10. Without offer_id it adds the offer the product page features (SATURN's own, or the featured Marketplace seller). With offer_id it adds that Marketplace seller's offer, picked in the product page's list of other offers: take product_id and offer_id from Get SATURN product offers. Returns the cart after the add (number of articles, total and currency, every line with its seller) and the product, offer and quantity that were added. A product the shop does not sell online, an offer that the product does not list, or a link that is not a product page fails with an error that says so. No sign-in needed; nothing is ordered or paid.

- Site: saturn.de
- Address: `reduck/saturn.de/add_to_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/saturn.de/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/saturn.de/add_to_cart
```

## Input

- `product` (string, required): SATURN product id (the product_id of Search SATURN products or Get SATURN product offers), or the product link.
- `offer_id` (string, optional): Marketplace offer id from Get SATURN product offers for this product. Leave it out to add the offer the product page features.
- `quantity` (integer, optional): Number of articles to add.

## Output

- `name` (string | null, required)
- `added` (integer, required): Number of articles added by this run.
- `count` (integer, required): Number of articles in the cart after the add.
- `lines` (array, required)
- `total` (number | null, required): Cart total, VAT included, before any shipping cost the checkout adds.
- `offerId` (string | null, required): Marketplace offer id that was added. Null when SATURN sells it.
- `currency` (string | null, required): Currency of the prices, EUR.
- `productId` (string, required): SATURN product id that was added.

## FAQ

### What does "Add a product to the SATURN cart" do?

Add a product to the guest shopping cart of this browser on SATURN Germany (saturn.de, the German store), by product id or product link, with a quantity from 1 to 10. Without offer_id it adds the offer the product page features (SATURN's own, or the featured Marketplace seller). With offer_id it adds that Marketplace seller's offer, picked in the product page's list of other offers: take product_id and offer_id from Get SATURN product offers. Returns the cart after the add (number of articles, total and currency, every line with its seller) and the product, offer and quantity that were added. A product the shop does not sell online, an offer that the product does not list, or a link that is not a product page fails with an error that says so. No sign-in needed; nothing is ordered or paid.

### How do I automatically add a product to the SATURN cart on saturn.de?

Ask an AI agent connected to Reduck to run reduck/saturn.de/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/saturn.de/add_to_cart

### Is there a saturn.de API to add a product to the SATURN cart?

You do not need one. "Add a product to the SATURN cart" drives the real saturn.de pages in a browser, so it works whether or not saturn.de offers an API for this.

### What information do I need to provide?

Required: product. Optional: offer_id, quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, currency, productId.

### Do I need to be logged in to saturn.de?

No. It only uses pages of saturn.de that are reachable without signing in.

### Does it change anything on saturn.de, or only read data?

It makes changes on saturn.de, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/saturn.de/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/saturn.de/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/saturn.de/add_to_cart
