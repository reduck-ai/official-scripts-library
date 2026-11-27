# Add a product to the dm cart

Automatically add a product to the dm cart on dm.de. Add a product to the guest shopping cart of this browser on dm Germany (dm.de, the German store), by product id or product link, with a quantity from 1 to 10. Returns the cart after the add (number of articles, value of the articles and currency, every line) and the product and quantity that were added. Prices are the online shop prices dm shows a new guest with no dm store chosen. A product the online shop does not sell now, an unknown product id, or a link that is not a product page fails with an error that says so. No sign-in needed; nothing is ordered or paid.

- Site: dm.de
- Address: `reduck/dm.de/add_to_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dm.de/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dm.de/add_to_cart
```

## Input

- `product` (string, required): dm product id (the product_id of Search dm products), or the product link.
- `quantity` (integer, optional): Number of articles to add.

## Output

- `name` (string | null, required)
- `added` (integer, required): Number of articles added by this run.
- `count` (integer, required): Number of articles in the cart after the add.
- `lines` (array, required)
- `total` (number | null, required): Value of the articles, VAT included, before the shipping cost the checkout adds.
- `offerId` (string | null, required): Always null: dm sells every product itself.
- `currency` (string | null, required): Currency of the prices, EUR.
- `productId` (string, required): dm product id that was added.

## FAQ

### What does "Add a product to the dm cart" do?

Add a product to the guest shopping cart of this browser on dm Germany (dm.de, the German store), by product id or product link, with a quantity from 1 to 10. Returns the cart after the add (number of articles, value of the articles and currency, every line) and the product and quantity that were added. Prices are the online shop prices dm shows a new guest with no dm store chosen. A product the online shop does not sell now, an unknown product id, or a link that is not a product page fails with an error that says so. No sign-in needed; nothing is ordered or paid.

### How do I automatically add a product to the dm cart on dm.de?

Ask an AI agent connected to Reduck to run reduck/dm.de/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dm.de/add_to_cart

### Is there a dm.de API to add a product to the dm cart?

You do not need one. "Add a product to the dm cart" drives the real dm.de pages in a browser, so it works whether or not dm.de offers an API for this.

### What information do I need to provide?

Required: product. Optional: quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, currency, productId.

### Do I need to be logged in to dm.de?

No. It only uses pages of dm.de that are reachable without signing in.

### Does it change anything on dm.de, or only read data?

It makes changes on dm.de, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dm.de/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dm.de/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/dm.de/add_to_cart
