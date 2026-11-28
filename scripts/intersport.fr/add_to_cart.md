# Add to Intersport cart

Automatically add to Intersport cart on intersport.fr. Add one size of an intersport.fr product to the basket.

- Site: intersport.fr
- Address: `reduck/intersport.fr/add_to_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/intersport.fr/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/intersport.fr/add_to_cart
```

## Input

- `product` (string, required): An intersport.fr product link or a code from search-products.
- `size` (string, optional): The size as get-product lists it (e.g. "42" or "M"). Needed when the product comes in several sizes.
- `quantity` (integer, optional)

## Output

- `sku` (string, required): Code of the size added
- `added` (integer, required)
- `review_hash` (string, required)
- `quantity_in_cart` (integer, required)
- `name` (string | null, optional)
- `size` (string | null, optional)
- `line_price` (number | null, optional)
- `unit_price` (number | null, optional)
- `cart_item_count` (integer, optional)

## FAQ

### What does "Add to Intersport cart" do?

Add one size of an intersport.fr product to the basket.

### How do I automatically add to Intersport cart on intersport.fr?

Ask an AI agent connected to Reduck to run reduck/intersport.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/intersport.fr/add_to_cart

### Is there a intersport.fr API to add to Intersport cart?

You do not need one. "Add to Intersport cart" drives the real intersport.fr pages in a browser, so it works whether or not intersport.fr offers an API for this.

### What information do I need to provide?

Required: product. Optional: size, quantity.

### What does it return?

It returns sku, name, size, added, line_price, unit_price, review_hash, cart_item_count, quantity_in_cart.

### Do I need to be logged in to intersport.fr?

No. It only uses pages of intersport.fr that are reachable without signing in.

### Does it change anything on intersport.fr, or only read data?

It makes changes on intersport.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/intersport.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/intersport.fr/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/intersport.fr/add_to_cart
