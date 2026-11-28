# Add to Monoprix cart

Automatically add to Monoprix cart on monoprix.fr. Add a product to the courses.monoprix.fr basket.

- Site: monoprix.fr
- Address: `reduck/monoprix.fr/add_to_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/monoprix.fr/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/monoprix.fr/add_to_cart
```

## Input

- `product` (string, required): A courses.monoprix.fr product link, or its id like MPX_6600978.
- `quantity` (integer, optional): How many units to add.

## Output

- `added` (integer, required): Units this run added
- `product_id` (string, required)
- `review_hash` (string, required): The line's hash as it is now, for remove_from_cart
- `quantity_in_cart` (integer, required): Units of this product in the basket now
- `name` (string | null, optional)
- `currency` (string | null, optional)
- `cart_total` (number | null, optional)
- `line_price` (number | null, optional)
- `unit_price` (number | null, optional)
- `cart_item_count` (integer, optional)

## FAQ

### What does "Add to Monoprix cart" do?

Add a product to the courses.monoprix.fr basket.

### How do I automatically add to Monoprix cart on monoprix.fr?

Ask an AI agent connected to Reduck to run reduck/monoprix.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/monoprix.fr/add_to_cart

### Is there a monoprix.fr API to add to Monoprix cart?

You do not need one. "Add to Monoprix cart" drives the real monoprix.fr pages in a browser, so it works whether or not monoprix.fr offers an API for this.

### What information do I need to provide?

Required: product. Optional: quantity.

### What does it return?

It returns name, added, currency, cart_total, line_price, product_id, unit_price, review_hash, cart_item_count, quantity_in_cart.

### Do I need to be logged in to monoprix.fr?

No. It only uses pages of monoprix.fr that are reachable without signing in.

### Does it change anything on monoprix.fr, or only read data?

It makes changes on monoprix.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/monoprix.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/monoprix.fr/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/monoprix.fr/add_to_cart
