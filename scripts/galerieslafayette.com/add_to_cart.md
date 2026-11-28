# Add to Galeries Lafayette cart

Automatically add to Galeries Lafayette cart on galerieslafayette.com. Add one size of a galerieslafayette.com product to the basket, from the best offer or a chosen seller.

- Site: galerieslafayette.com
- Address: `reduck/galerieslafayette.com/add_to_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/galerieslafayette.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/galerieslafayette.com/add_to_cart
```

## Input

- `product` (string, required): A galerieslafayette.com product link or a code from search-products or get-product.
- `size` (string, optional): The size, as get-product lists it (e.g. "M"). Needed when the colour comes in several sizes.
- `offer_id` (string, optional): A seller's offer_id from get-product-offers. Leave out for the best offer (or Galeries Lafayette's own stock).
- `quantity` (integer, optional)

## Output

- `added` (integer, required)
- `product_id` (string, required): Code of the size added
- `review_hash` (string, required)
- `quantity_in_cart` (integer, required)
- `name` (string | null, optional)
- `size` (string | null, optional)
- `color` (string | null, optional)
- `seller` (string | null, optional)
- `offer_id` (string | null, optional)
- `cart_total` (number | null, optional)
- `line_price` (number | null, optional)
- `unit_price` (number | null, optional)
- `cart_item_count` (integer, optional)

## FAQ

### What does "Add to Galeries Lafayette cart" do?

Add one size of a galerieslafayette.com product to the basket, from the best offer or a chosen seller.

### How do I automatically add to Galeries Lafayette cart on galerieslafayette.com?

Ask an AI agent connected to Reduck to run reduck/galerieslafayette.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/galerieslafayette.com/add_to_cart

### Is there a galerieslafayette.com API to add to Galeries Lafayette cart?

You do not need one. "Add to Galeries Lafayette cart" drives the real galerieslafayette.com pages in a browser, so it works whether or not galerieslafayette.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: size, offer_id, quantity.

### What does it return?

It returns name, size, added, color, seller, offer_id, cart_total, line_price, product_id, unit_price, review_hash, cart_item_count, quantity_in_cart.

### Do I need to be logged in to galerieslafayette.com?

No. It only uses pages of galerieslafayette.com that are reachable without signing in.

### Does it change anything on galerieslafayette.com, or only read data?

It makes changes on galerieslafayette.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/galerieslafayette.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/galerieslafayette.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/galerieslafayette.com/add_to_cart
