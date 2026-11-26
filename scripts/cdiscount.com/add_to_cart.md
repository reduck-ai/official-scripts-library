# Add to Cdiscount cart

Automatically add to Cdiscount cart on cdiscount.com. Add 1 to 10 units of a Cdiscount.com product to the cart, from its sku, from the offer the product page shows or from a given seller's offer (offer_id from Get Cdiscount product offers), and return the cart after the add. Works as a guest: the cart lives with the browser. Nothing is paid or ordered. An unknown sku or an offer_id the product does not have is refused with a clear message.

- Site: cdiscount.com
- Address: `reduck/cdiscount.com/add_to_cart`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cdiscount.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cdiscount.com/add_to_cart
```

## Input

- `sku` (string, required): Cdiscount product id, for example aaaqy27804.
- `offer_id` (string, optional): A seller's offer from Get Cdiscount product offers. Omit for the offer the product page shows first.
- `quantity` (integer, optional)

## Output

- `sku` (string, required)
- `cart` (object, required)
- `added` (integer, required)
- `offer_id` (string, required)

## FAQ

### What does "Add to Cdiscount cart" do?

Add 1 to 10 units of a Cdiscount.com product to the cart, from its sku, from the offer the product page shows or from a given seller's offer (offer_id from Get Cdiscount product offers), and return the cart after the add. Works as a guest: the cart lives with the browser. Nothing is paid or ordered. An unknown sku or an offer_id the product does not have is refused with a clear message.

### How do I automatically add to Cdiscount cart on cdiscount.com?

Ask an AI agent connected to Reduck to run reduck/cdiscount.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cdiscount.com/add_to_cart

### Is there a cdiscount.com API to add to Cdiscount cart?

You do not need one. "Add to Cdiscount cart" drives the real cdiscount.com pages in a browser, so it works whether or not cdiscount.com offers an API for this.

### What information do I need to provide?

Required: sku. Optional: offer_id, quantity.

### What does it return?

It returns sku, cart, added, offer_id.

### Do I need to be logged in to cdiscount.com?

No. It only uses pages of cdiscount.com that are reachable without signing in.

### Does it change anything on cdiscount.com, or only read data?

It makes changes on cdiscount.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cdiscount.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cdiscount.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/cdiscount.com/add_to_cart
