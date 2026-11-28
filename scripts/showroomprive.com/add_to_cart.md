# Add to Showroomprivé cart

Automatically add to Showroomprivé cart on showroomprive.com. Add one size of a showroomprive.com product to the signed-in member's basket.

- Site: showroomprive.com
- Address: `reduck/showroomprive.com/add_to_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/showroomprive.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/showroomprive.com/add_to_cart
```

## Input

- `product` (string, required): A showroomprive.com product link or a product id from search-products.
- `size` (string, optional): The size label (e.g. "40" or "M") or its size_id, as get-product lists them. Needed when the product has several sizes.
- `quantity` (integer, optional)

## Output

- `added` (integer, required)
- `size_id` (integer, required)
- `product_id` (string, required)
- `review_hash` (string, required)
- `quantity_in_cart` (integer, required)
- `name` (string | null, optional)
- `size` (string | null, optional)
- `cart_total` (number | null, optional)
- `line_price` (number | null, optional)
- `unit_price` (number | null, optional)
- `cart_item_count` (integer, optional)
- `reserved_for_seconds` (integer | null, optional)

## FAQ

### What does "Add to Showroomprivé cart" do?

Add one size of a showroomprive.com product to the signed-in member's basket.

### How do I automatically add to Showroomprivé cart on showroomprive.com?

Ask an AI agent connected to Reduck to run reduck/showroomprive.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/showroomprive.com/add_to_cart

### Is there a showroomprive.com API to add to Showroomprivé cart?

You do not need one. "Add to Showroomprivé cart" drives the real showroomprive.com pages in a browser, so it works whether or not showroomprive.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: size, quantity.

### What does it return?

It returns name, size, added, size_id, cart_total, line_price, product_id, unit_price, review_hash, cart_item_count, quantity_in_cart, reserved_for_seconds.

### Do I need to be logged in to showroomprive.com?

Yes. It acts as you on showroomprive.com: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for showroomprive.com.

### Does it change anything on showroomprive.com, or only read data?

It makes changes on showroomprive.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/showroomprive.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/showroomprive.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/showroomprive.com/add_to_cart
