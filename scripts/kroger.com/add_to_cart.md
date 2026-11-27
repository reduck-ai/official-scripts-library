# Add to Kroger cart

Automatically add to Kroger cart on kroger.com. Add a Kroger.com product to the signed-in cart for pickup, by UPC, in the given quantity (added to any already in the cart). Returns the cart as it is after the add, with a review_hash per line. Refuses a product the store cannot sell for pickup, or a product Kroger does not have.

- Site: kroger.com
- Address: `reduck/kroger.com/add_to_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/kroger.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/kroger.com/add_to_cart
```

## Input

- `product` (string, required): A 13-digit Kroger UPC or a product link ending in it, from Search Kroger products.
- `quantity` (integer, optional)

## Output

- `added` (object, required)
- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, optional)

## FAQ

### What does "Add to Kroger cart" do?

Add a Kroger.com product to the signed-in cart for pickup, by UPC, in the given quantity (added to any already in the cart). Returns the cart as it is after the add, with a review_hash per line. Refuses a product the store cannot sell for pickup, or a product Kroger does not have.

### How do I automatically add to Kroger cart on kroger.com?

Ask an AI agent connected to Reduck to run reduck/kroger.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kroger.com/add_to_cart

### Is there a kroger.com API to add to Kroger cart?

You do not need one. "Add to Kroger cart" drives the real kroger.com pages in a browser, so it works whether or not kroger.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: quantity.

### What does it return?

It returns added, count, lines, total.

### Do I need to be logged in to kroger.com?

Yes. It acts as you on kroger.com: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for kroger.com.

### Does it change anything on kroger.com, or only read data?

It makes changes on kroger.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/kroger.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kroger.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/kroger.com/add_to_cart
