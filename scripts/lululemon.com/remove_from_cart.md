# Remove from lululemon cart

Automatically remove from lululemon cart on lululemon.com. Remove one line from the shop.lululemon.com bag, after checking it is still the line you reviewed.

- Site: lululemon.com
- Address: `reduck/lululemon.com/remove_from_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/lululemon.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/lululemon.com/remove_from_cart
```

## Input

- `item_id` (string, required): The line's item_id from list_cart_items.
- `review_hash` (string, required): The line's review_hash from list_cart_items or add_to_cart. The removal is refused if the line changed since.

## Output

- `item_id` (string, required)
- `cart_item_count` (integer, required)
- `removed_quantity` (integer, required)
- `sku` (string, optional)
- `name` (string | null, optional)
- `cart_subtotal` (number | null, optional)

## FAQ

### What does "Remove from lululemon cart" do?

Remove one line from the shop.lululemon.com bag, after checking it is still the line you reviewed.

### How do I automatically remove from lululemon cart on lululemon.com?

Ask an AI agent connected to Reduck to run reduck/lululemon.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lululemon.com/remove_from_cart

### Is there a lululemon.com API to remove from lululemon cart?

You do not need one. "Remove from lululemon cart" drives the real lululemon.com pages in a browser, so it works whether or not lululemon.com offers an API for this.

### What information do I need to provide?

Required: item_id, review_hash.

### What does it return?

It returns sku, name, item_id, cart_subtotal, cart_item_count, removed_quantity.

### Do I need to be logged in to lululemon.com?

No. It only uses pages of lululemon.com that are reachable without signing in.

### Does it change anything on lululemon.com, or only read data?

It makes changes on lululemon.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/lululemon.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lululemon.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/lululemon.com/remove_from_cart
