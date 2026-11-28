# Remove from Monoprix cart

Automatically remove from Monoprix cart on monoprix.fr. Remove a product line from the courses.monoprix.fr basket, after checking it is still the line you reviewed.

- Site: monoprix.fr
- Address: `reduck/monoprix.fr/remove_from_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/monoprix.fr/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/monoprix.fr/remove_from_cart
```

## Input

- `product_id` (string, required): The line's MPX_… id (or product link), from list_cart_items.
- `review_hash` (string, required): The line's review_hash from list_cart_items or add_to_cart. The removal is refused if the line changed since.

## Output

- `product_id` (string, required)
- `cart_item_count` (integer, required)
- `removed_quantity` (integer, required)
- `name` (string | null, optional)
- `cart_total` (number | null, optional)

## FAQ

### What does "Remove from Monoprix cart" do?

Remove a product line from the courses.monoprix.fr basket, after checking it is still the line you reviewed.

### How do I automatically remove from Monoprix cart on monoprix.fr?

Ask an AI agent connected to Reduck to run reduck/monoprix.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/monoprix.fr/remove_from_cart

### Is there a monoprix.fr API to remove from Monoprix cart?

You do not need one. "Remove from Monoprix cart" drives the real monoprix.fr pages in a browser, so it works whether or not monoprix.fr offers an API for this.

### What information do I need to provide?

Required: product_id, review_hash.

### What does it return?

It returns name, cart_total, product_id, cart_item_count, removed_quantity.

### Do I need to be logged in to monoprix.fr?

No. It only uses pages of monoprix.fr that are reachable without signing in.

### Does it change anything on monoprix.fr, or only read data?

It makes changes on monoprix.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/monoprix.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/monoprix.fr/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/monoprix.fr/remove_from_cart
