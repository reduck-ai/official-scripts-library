# Remove from Galeries Lafayette cart

Automatically remove from Galeries Lafayette cart on galerieslafayette.com. Remove one line from the galerieslafayette.com basket, after checking it is still the line you reviewed.

- Site: galerieslafayette.com
- Address: `reduck/galerieslafayette.com/remove_from_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/galerieslafayette.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/galerieslafayette.com/remove_from_cart
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

### What does "Remove from Galeries Lafayette cart" do?

Remove one line from the galerieslafayette.com basket, after checking it is still the line you reviewed.

### How do I automatically remove from Galeries Lafayette cart on galerieslafayette.com?

Ask an AI agent connected to Reduck to run reduck/galerieslafayette.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/galerieslafayette.com/remove_from_cart

### Is there a galerieslafayette.com API to remove from Galeries Lafayette cart?

You do not need one. "Remove from Galeries Lafayette cart" drives the real galerieslafayette.com pages in a browser, so it works whether or not galerieslafayette.com offers an API for this.

### What information do I need to provide?

Required: product_id, review_hash.

### What does it return?

It returns name, cart_total, product_id, cart_item_count, removed_quantity.

### Do I need to be logged in to galerieslafayette.com?

No. It only uses pages of galerieslafayette.com that are reachable without signing in.

### Does it change anything on galerieslafayette.com, or only read data?

It makes changes on galerieslafayette.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/galerieslafayette.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/galerieslafayette.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/galerieslafayette.com/remove_from_cart
