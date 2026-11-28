# Remove from E.Leclerc cart

Automatically remove from E.Leclerc cart on e.leclerc. Remove one offer line from the e.leclerc basket, after checking it is still the line you reviewed.

- Site: e.leclerc
- Address: `reduck/e.leclerc/remove_from_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/e.leclerc/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/e.leclerc/remove_from_cart
```

## Input

- `offer_id` (string, required): The line's offer_id from list_cart_items.
- `product_id` (string, required): The line's product_id (barcode number) from list_cart_items, or the product link.
- `review_hash` (string, required): The line's review_hash from list_cart_items or add_to_cart. The removal is refused if the line changed since.

## Output

- `offer_id` (string, required)
- `product_id` (string, required)
- `cart_item_count` (integer, required)
- `removed_quantity` (integer, required)
- `name` (string | null, optional)
- `cart_total` (number | null, optional)

## FAQ

### What does "Remove from E.Leclerc cart" do?

Remove one offer line from the e.leclerc basket, after checking it is still the line you reviewed.

### How do I automatically remove from E.Leclerc cart on e.leclerc?

Ask an AI agent connected to Reduck to run reduck/e.leclerc/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/e.leclerc/remove_from_cart

### Is there a e.leclerc API to remove from E.Leclerc cart?

You do not need one. "Remove from E.Leclerc cart" drives the real e.leclerc pages in a browser, so it works whether or not e.leclerc offers an API for this.

### What information do I need to provide?

Required: product_id, offer_id, review_hash.

### What does it return?

It returns name, offer_id, cart_total, product_id, cart_item_count, removed_quantity.

### Do I need to be logged in to e.leclerc?

No. It only uses pages of e.leclerc that are reachable without signing in.

### Does it change anything on e.leclerc, or only read data?

It makes changes on e.leclerc, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/e.leclerc/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/e.leclerc/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/e.leclerc/remove_from_cart
