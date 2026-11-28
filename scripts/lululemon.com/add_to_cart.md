# Add to lululemon cart

Automatically add to lululemon cart on lululemon.com. Add one colour and size of a shop.lululemon.com product to the bag.

- Site: lululemon.com
- Address: `reduck/lululemon.com/add_to_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/lululemon.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/lululemon.com/add_to_cart
```

## Input

- `product` (string, required): A shop.lululemon.com product link or a product id from search-products.
- `sku` (string, optional): A sku from get-product's variants. Or pass color and size instead.
- `size` (string, optional): The size, as get-product lists it (e.g. "6" or "M").
- `color` (string, optional): The colour name, as get-product lists it.
- `quantity` (integer, optional)

## Output

- `sku` (string, required)
- `added` (integer, required)
- `review_hash` (string, required)
- `quantity_in_cart` (integer, required)
- `name` (string | null, optional)
- `size` (string | null, optional)
- `color` (string | null, optional)
- `item_id` (string, optional)
- `product_id` (string, optional)
- `unit_price` (number | null, optional)
- `cart_subtotal` (number | null, optional)
- `cart_item_count` (integer, optional)

## FAQ

### What does "Add to lululemon cart" do?

Add one colour and size of a shop.lululemon.com product to the bag.

### How do I automatically add to lululemon cart on lululemon.com?

Ask an AI agent connected to Reduck to run reduck/lululemon.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lululemon.com/add_to_cart

### Is there a lululemon.com API to add to lululemon cart?

You do not need one. "Add to lululemon cart" drives the real lululemon.com pages in a browser, so it works whether or not lululemon.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: sku, size, color, quantity.

### What does it return?

It returns sku, name, size, added, color, item_id, product_id, unit_price, review_hash, cart_subtotal, cart_item_count, quantity_in_cart.

### Do I need to be logged in to lululemon.com?

No. It only uses pages of lululemon.com that are reachable without signing in.

### Does it change anything on lululemon.com, or only read data?

It makes changes on lululemon.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/lululemon.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lululemon.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/lululemon.com/add_to_cart
