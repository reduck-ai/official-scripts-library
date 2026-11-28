# Remove a product from the Holland & Barrett cart

Automatically remove a product from the Holland & Barrett cart on hollandandbarrett.com. Remove a product from the basket of this browser on Holland & Barrett UK (hollandandbarrett.com, the United Kingdom store), from its Holland & Barrett product id or product page link, whatever its quantity, with the basket page's own quantity button. Returns removed and the basket after it: each line with its product id, sku, name, seller, quantity, unit price and line price in pounds (GBP), the item count, the total and the currency. A product that is not in the basket gives removed false and the basket unchanged, not an error. Works as a guest, with no account.

- Site: hollandandbarrett.com
- Address: `reduck/hollandandbarrett.com/remove_from_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hollandandbarrett.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hollandandbarrett.com/remove_from_cart
```

## Input

- `product` (string, required): A Holland & Barrett product id as List Holland & Barrett cart items returns it, for example 6100005252, or a hollandandbarrett.com product page link.

## Output

- `count` (integer, required): Units in the basket after the removal.
- `lines` (array, required)
- `total` (number | null, required)
- `removed` (boolean, required): True when this run removed the product, false when it was not in the basket.
- `currency` (string | null, required)

## FAQ

### What does "Remove a product from the Holland & Barrett cart" do?

Remove a product from the basket of this browser on Holland & Barrett UK (hollandandbarrett.com, the United Kingdom store), from its Holland & Barrett product id or product page link, whatever its quantity, with the basket page's own quantity button. Returns removed and the basket after it: each line with its product id, sku, name, seller, quantity, unit price and line price in pounds (GBP), the item count, the total and the currency. A product that is not in the basket gives removed false and the basket unchanged, not an error. Works as a guest, with no account.

### How do I automatically remove a product from the Holland & Barrett cart on hollandandbarrett.com?

Ask an AI agent connected to Reduck to run reduck/hollandandbarrett.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hollandandbarrett.com/remove_from_cart

### Is there a hollandandbarrett.com API to remove a product from the Holland & Barrett cart?

You do not need one. "Remove a product from the Holland & Barrett cart" drives the real hollandandbarrett.com pages in a browser, so it works whether or not hollandandbarrett.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns count, lines, total, removed, currency.

### Do I need to be logged in to hollandandbarrett.com?

No. It only uses pages of hollandandbarrett.com that are reachable without signing in.

### Does it change anything on hollandandbarrett.com, or only read data?

It makes changes on hollandandbarrett.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hollandandbarrett.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hollandandbarrett.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/hollandandbarrett.com/remove_from_cart
