# Remove a product from the JD Sports cart

Automatically remove a product from the JD Sports cart on jdsports.co.uk. Remove a product from the shopping bag of this browser on JD Sports UK (jdsports.co.uk, the United Kingdom store), from its JD Sports product id or product page link, whatever its quantity, as the bag page's delete button does: every line of the product, or only the lines of one size when you pass its sku (offerId). Returns removed and the bag after it: each line with its line id, product id, size sku, name, size, quantity, unit price and line price in pounds (GBP), the item count, the total, the subtotal and the currency. A product that is not in the bag gives removed false and the bag unchanged, not an error. Works as a guest, with no account.

- Site: jdsports.co.uk
- Address: `reduck/jdsports.co.uk/remove_from_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/jdsports.co.uk/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/jdsports.co.uk/remove_from_cart
```

## Input

- `product` (string, required): A JD Sports product id as List JD Sports cart items returns it, for example 19760893, or a jdsports.co.uk product page link.
- `offerId` (string, optional): Remove only the lines of this size sku (from List JD Sports cart items). Leave it out to remove every size of the product.

## Output

- `count` (integer, required): Units in the bag after the removal.
- `lines` (array, required)
- `total` (number | null, required)
- `removed` (boolean, required): True when this run removed lines, false when the product was not in the bag.
- `currency` (string | null, required)
- `subtotal` (number | null, required)

## FAQ

### What does "Remove a product from the JD Sports cart" do?

Remove a product from the shopping bag of this browser on JD Sports UK (jdsports.co.uk, the United Kingdom store), from its JD Sports product id or product page link, whatever its quantity, as the bag page's delete button does: every line of the product, or only the lines of one size when you pass its sku (offerId). Returns removed and the bag after it: each line with its line id, product id, size sku, name, size, quantity, unit price and line price in pounds (GBP), the item count, the total, the subtotal and the currency. A product that is not in the bag gives removed false and the bag unchanged, not an error. Works as a guest, with no account.

### How do I automatically remove a product from the JD Sports cart on jdsports.co.uk?

Ask an AI agent connected to Reduck to run reduck/jdsports.co.uk/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/jdsports.co.uk/remove_from_cart

### Is there a jdsports.co.uk API to remove a product from the JD Sports cart?

You do not need one. "Remove a product from the JD Sports cart" drives the real jdsports.co.uk pages in a browser, so it works whether or not jdsports.co.uk offers an API for this.

### What information do I need to provide?

Required: product. Optional: offerId.

### What does it return?

It returns count, lines, total, removed, currency, subtotal.

### Do I need to be logged in to jdsports.co.uk?

No. It only uses pages of jdsports.co.uk that are reachable without signing in.

### Does it change anything on jdsports.co.uk, or only read data?

It makes changes on jdsports.co.uk, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/jdsports.co.uk/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/jdsports.co.uk/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/jdsports.co.uk/remove_from_cart
