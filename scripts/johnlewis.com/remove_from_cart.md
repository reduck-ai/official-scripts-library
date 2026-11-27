# Remove John Lewis product from basket

Automatically remove John Lewis product from basket on johnlewis.com. Remove a product from the John Lewis UK store (johnlewis.com) basket of this browser by its product id (the sku id, as returned by List John Lewis basket items), whatever its quantity, and return what is left in the basket: each line with its line id, product id, offer id, name with the brand, seller, quantity, unit price and line price, plus the item count, the basket total and the currency (GBP). A product that is not in the basket is reported with removed false and the basket unchanged, not as a failure. Works as a guest, with no account.

- Site: johnlewis.com
- Address: `reduck/johnlewis.com/remove_from_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/johnlewis.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/johnlewis.com/remove_from_cart
```

## Input

- `product_id` (string, required): Sku id of the line to remove: productId of List John Lewis basket items or Add John Lewis product to basket.

## Output

- `count` (integer, required): Number of units left in the basket.
- `lines` (array, required)
- `total` (number | null, required): Basket subtotal before delivery, in pounds sterling.
- `removed` (boolean, required): True when the product was in the basket and is gone now; false when it was not in the basket.
- `currency` (string, required): GBP

## FAQ

### What does "Remove John Lewis product from basket" do?

Remove a product from the John Lewis UK store (johnlewis.com) basket of this browser by its product id (the sku id, as returned by List John Lewis basket items), whatever its quantity, and return what is left in the basket: each line with its line id, product id, offer id, name with the brand, seller, quantity, unit price and line price, plus the item count, the basket total and the currency (GBP). A product that is not in the basket is reported with removed false and the basket unchanged, not as a failure. Works as a guest, with no account.

### How do I automatically remove John Lewis product from basket on johnlewis.com?

Ask an AI agent connected to Reduck to run reduck/johnlewis.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/johnlewis.com/remove_from_cart

### Is there a johnlewis.com API to remove John Lewis product from basket?

You do not need one. "Remove John Lewis product from basket" drives the real johnlewis.com pages in a browser, so it works whether or not johnlewis.com offers an API for this.

### What information do I need to provide?

Required: product_id.

### What does it return?

It returns count, lines, total, removed, currency.

### Do I need to be logged in to johnlewis.com?

No. It only uses pages of johnlewis.com that are reachable without signing in.

### Does it change anything on johnlewis.com, or only read data?

It makes changes on johnlewis.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/johnlewis.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/johnlewis.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/johnlewis.com/remove_from_cart
