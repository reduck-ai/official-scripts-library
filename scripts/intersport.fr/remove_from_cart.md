# Remove from Intersport cart

Automatically remove from Intersport cart on intersport.fr. Remove one size line from the intersport.fr basket, after checking it is still the line you reviewed.

- Site: intersport.fr
- Address: `reduck/intersport.fr/remove_from_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/intersport.fr/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/intersport.fr/remove_from_cart
```

## Input

- `sku` (string, required): The line's sku from list_cart_items.
- `review_hash` (string, required): The line's review_hash from list_cart_items or add_to_cart. The removal is refused if the line changed since.

## Output

- `sku` (string, required)
- `cart_item_count` (integer, required)
- `removed_quantity` (integer, required)
- `name` (string | null, optional)

## FAQ

### What does "Remove from Intersport cart" do?

Remove one size line from the intersport.fr basket, after checking it is still the line you reviewed.

### How do I automatically remove from Intersport cart on intersport.fr?

Ask an AI agent connected to Reduck to run reduck/intersport.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/intersport.fr/remove_from_cart

### Is there a intersport.fr API to remove from Intersport cart?

You do not need one. "Remove from Intersport cart" drives the real intersport.fr pages in a browser, so it works whether or not intersport.fr offers an API for this.

### What information do I need to provide?

Required: sku, review_hash.

### What does it return?

It returns sku, name, cart_item_count, removed_quantity.

### Do I need to be logged in to intersport.fr?

No. It only uses pages of intersport.fr that are reachable without signing in.

### Does it change anything on intersport.fr, or only read data?

It makes changes on intersport.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/intersport.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/intersport.fr/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/intersport.fr/remove_from_cart
