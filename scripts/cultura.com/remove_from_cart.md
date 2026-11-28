# Remove from Cultura cart

Automatically remove from Cultura cart on cultura.com. Remove one line from the cultura.com basket, after checking it is still the line you reviewed.

- Site: cultura.com
- Address: `reduck/cultura.com/remove_from_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cultura.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cultura.com/remove_from_cart
```

## Input

- `product_id` (string, required): The line's product_id from list_cart_items.
- `review_hash` (string, required): The line's review_hash from list_cart_items or add_to_cart. The removal is refused if the line changed since.

## Output

- `product_id` (string, required)
- `cart_item_count` (integer, required)
- `removed_quantity` (integer, required)
- `name` (string | null, optional)
- `cart_total` (number | null, optional)

## FAQ

### What does "Remove from Cultura cart" do?

Remove one line from the cultura.com basket, after checking it is still the line you reviewed.

### How do I automatically remove from Cultura cart on cultura.com?

Ask an AI agent connected to Reduck to run reduck/cultura.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cultura.com/remove_from_cart

### Is there a cultura.com API to remove from Cultura cart?

You do not need one. "Remove from Cultura cart" drives the real cultura.com pages in a browser, so it works whether or not cultura.com offers an API for this.

### What information do I need to provide?

Required: product_id, review_hash.

### What does it return?

It returns name, cart_total, product_id, cart_item_count, removed_quantity.

### Do I need to be logged in to cultura.com?

No. It only uses pages of cultura.com that are reachable without signing in.

### Does it change anything on cultura.com, or only read data?

It makes changes on cultura.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cultura.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cultura.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/cultura.com/remove_from_cart
