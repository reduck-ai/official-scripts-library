# Remove a product from the Nocibé cart

Automatically remove a product from the Nocibé cart on nocibe.fr. Remove one line from the Nocibé (nocibe.fr) cart of this browser, whatever its quantity, as the cart page does. Pass the line's item_id and review_hash from List Nocibé cart items: the removal is refused when the line changed since it was read (another quantity or price), and an item that is not in the cart is refused too, so nothing else is ever removed. Returns the item removed, its name, the units removed, and the cart's count and subtotal in euros afterwards. Works as a guest, with no account. Works in your own browser (the extension); Nocibé refuses cloud browsers.

- Site: nocibe.fr
- Address: `reduck/nocibe.fr/remove_from_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/nocibe.fr/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/nocibe.fr/remove_from_cart
```

## Input

- `item_id` (string, required): item_id of the line, from List Nocibé cart items.
- `review_hash` (string, required): review_hash of the same line, from List Nocibé cart items. The removal is refused when the line changed since it was read.

## Output

- `item_id` (string, required)
- `removed_quantity` (integer, required)
- `name` (string | null, optional)
- `currency` (string, optional)
- `cart_count` (integer, optional)
- `cart_subtotal` (number, optional)

## FAQ

### What does "Remove a product from the Nocibé cart" do?

Remove one line from the Nocibé (nocibe.fr) cart of this browser, whatever its quantity, as the cart page does. Pass the line's item_id and review_hash from List Nocibé cart items: the removal is refused when the line changed since it was read (another quantity or price), and an item that is not in the cart is refused too, so nothing else is ever removed. Returns the item removed, its name, the units removed, and the cart's count and subtotal in euros afterwards. Works as a guest, with no account. Works in your own browser (the extension); Nocibé refuses cloud browsers.

### How do I automatically remove a product from the Nocibé cart on nocibe.fr?

Ask an AI agent connected to Reduck to run reduck/nocibe.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/nocibe.fr/remove_from_cart

### Is there a nocibe.fr API to remove a product from the Nocibé cart?

You do not need one. "Remove a product from the Nocibé cart" drives the real nocibe.fr pages in a browser, so it works whether or not nocibe.fr offers an API for this.

### What information do I need to provide?

Required: item_id, review_hash.

### What does it return?

It returns name, item_id, currency, cart_count, cart_subtotal, removed_quantity.

### Do I need to be logged in to nocibe.fr?

No. It only uses pages of nocibe.fr that are reachable without signing in.

### Does it change anything on nocibe.fr, or only read data?

It makes changes on nocibe.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/nocibe.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/nocibe.fr/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/nocibe.fr/remove_from_cart
