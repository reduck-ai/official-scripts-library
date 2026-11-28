# Remove from Showroomprivé cart

Automatically remove from Showroomprivé cart on showroomprive.com. Remove one size line from the signed-in member's showroomprive.com basket, after checking it is still the line you reviewed.

- Site: showroomprive.com
- Address: `reduck/showroomprive.com/remove_from_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/showroomprive.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/showroomprive.com/remove_from_cart
```

## Input

- `size_id` (integer, required): The line's size_id from list_cart_items.
- `product_id` (string, required): The line's product_id from list_cart_items.
- `review_hash` (string, required): The line's review_hash from list_cart_items or add_to_cart. The removal is refused if the line changed since.

## Output

- `size_id` (integer, required)
- `product_id` (string, required)
- `cart_item_count` (integer, required)
- `removed_quantity` (integer, required)
- `name` (string | null, optional)
- `cart_total` (number | null, optional)

## FAQ

### What does "Remove from Showroomprivé cart" do?

Remove one size line from the signed-in member's showroomprive.com basket, after checking it is still the line you reviewed.

### How do I automatically remove from Showroomprivé cart on showroomprive.com?

Ask an AI agent connected to Reduck to run reduck/showroomprive.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/showroomprive.com/remove_from_cart

### Is there a showroomprive.com API to remove from Showroomprivé cart?

You do not need one. "Remove from Showroomprivé cart" drives the real showroomprive.com pages in a browser, so it works whether or not showroomprive.com offers an API for this.

### What information do I need to provide?

Required: product_id, size_id, review_hash.

### What does it return?

It returns name, size_id, cart_total, product_id, cart_item_count, removed_quantity.

### Do I need to be logged in to showroomprive.com?

Yes. It acts as you on showroomprive.com: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for showroomprive.com.

### Does it change anything on showroomprive.com, or only read data?

It makes changes on showroomprive.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/showroomprive.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/showroomprive.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/showroomprive.com/remove_from_cart
