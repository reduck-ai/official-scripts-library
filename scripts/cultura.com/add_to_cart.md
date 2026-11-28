# Add to Cultura cart

Automatically add to Cultura cart on cultura.com. Add a cultura.com product to the basket, from Cultura or a chosen marketplace seller's offer.

- Site: cultura.com
- Address: `reduck/cultura.com/add_to_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cultura.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cultura.com/add_to_cart
```

## Input

- `product` (string, required): A cultura.com product link or a product id from search-products.
- `offer_id` (integer, optional): A marketplace seller's offer_id from get-product-offers. Leave out to buy from Cultura.
- `quantity` (integer, optional)

## Output

- `added` (integer, required)
- `product_id` (string, required)
- `review_hash` (string, required)
- `quantity_in_cart` (integer, required)
- `name` (string | null, optional)
- `seller` (string | null, optional)
- `offer_id` (integer | null, optional)
- `cart_total` (number | null, optional)
- `line_price` (number | null, optional)
- `unit_price` (number | null, optional)
- `cart_item_count` (integer, optional)

## FAQ

### What does "Add to Cultura cart" do?

Add a cultura.com product to the basket, from Cultura or a chosen marketplace seller's offer.

### How do I automatically add to Cultura cart on cultura.com?

Ask an AI agent connected to Reduck to run reduck/cultura.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cultura.com/add_to_cart

### Is there a cultura.com API to add to Cultura cart?

You do not need one. "Add to Cultura cart" drives the real cultura.com pages in a browser, so it works whether or not cultura.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: offer_id, quantity.

### What does it return?

It returns name, added, seller, offer_id, cart_total, line_price, product_id, unit_price, review_hash, cart_item_count, quantity_in_cart.

### Do I need to be logged in to cultura.com?

No. It only uses pages of cultura.com that are reachable without signing in.

### Does it change anything on cultura.com, or only read data?

It makes changes on cultura.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cultura.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cultura.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/cultura.com/add_to_cart
