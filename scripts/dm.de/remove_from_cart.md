# Remove a product from the dm cart

Automatically remove a product from the dm cart on dm.de. Remove a product from the guest shopping cart of this browser on dm Germany (dm.de, the German store), by product id or product link, whatever its quantity. Returns the cart after the removal (number of articles, value of the articles and currency, every line) and removed true; a product that is not in the cart leaves the cart as it is and returns removed false. Other lines are never touched. No sign-in needed.

- Site: dm.de
- Address: `reduck/dm.de/remove_from_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dm.de/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dm.de/remove_from_cart
```

## Input

- `product` (string, required): dm product id as List dm cart items gives it (productId), or the product link.

## Output

- `count` (integer, required): Number of articles in the cart after the removal.
- `lines` (array, required)
- `total` (number | null, required): Value of the articles, VAT included, before the shipping cost the checkout adds.
- `removed` (boolean, required): True when the product was in the cart and is now gone.
- `currency` (string | null, required): Currency of the prices, EUR. Null for an empty cart, for which dm gives none.

## FAQ

### What does "Remove a product from the dm cart" do?

Remove a product from the guest shopping cart of this browser on dm Germany (dm.de, the German store), by product id or product link, whatever its quantity. Returns the cart after the removal (number of articles, value of the articles and currency, every line) and removed true; a product that is not in the cart leaves the cart as it is and returns removed false. Other lines are never touched. No sign-in needed.

### How do I automatically remove a product from the dm cart on dm.de?

Ask an AI agent connected to Reduck to run reduck/dm.de/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dm.de/remove_from_cart

### Is there a dm.de API to remove a product from the dm cart?

You do not need one. "Remove a product from the dm cart" drives the real dm.de pages in a browser, so it works whether or not dm.de offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns count, lines, total, removed, currency.

### Do I need to be logged in to dm.de?

No. It only uses pages of dm.de that are reachable without signing in.

### Does it change anything on dm.de, or only read data?

It makes changes on dm.de, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dm.de/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dm.de/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/dm.de/remove_from_cart
