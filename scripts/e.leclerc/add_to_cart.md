# Add to E.Leclerc cart

Automatically add to E.Leclerc cart on e.leclerc. Add a product to the e.leclerc basket, from the featured offer or a chosen seller's offer.

- Site: e.leclerc
- Address: `reduck/e.leclerc/add_to_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/e.leclerc/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/e.leclerc/add_to_cart
```

## Input

- `product` (string, required): An e.leclerc product link or the product's barcode number (id from search-products).
- `offer_id` (string, optional): A seller's offer_id from get-product-offers. Leave out for the offer e.leclerc shows first.
- `quantity` (integer, optional)

## Output

- `added` (integer, required)
- `offer_id` (string, required)
- `product_id` (string, required)
- `review_hash` (string, required)
- `quantity_in_cart` (integer, required)
- `name` (string | null, optional)
- `cart_total` (number | null, optional)
- `line_price` (number | null, optional)
- `unit_price` (number | null, optional)
- `cart_item_count` (integer, optional)

## FAQ

### What does "Add to E.Leclerc cart" do?

Add a product to the e.leclerc basket, from the featured offer or a chosen seller's offer.

### How do I automatically add to E.Leclerc cart on e.leclerc?

Ask an AI agent connected to Reduck to run reduck/e.leclerc/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/e.leclerc/add_to_cart

### Is there a e.leclerc API to add to E.Leclerc cart?

You do not need one. "Add to E.Leclerc cart" drives the real e.leclerc pages in a browser, so it works whether or not e.leclerc offers an API for this.

### What information do I need to provide?

Required: product. Optional: offer_id, quantity.

### What does it return?

It returns name, added, offer_id, cart_total, line_price, product_id, unit_price, review_hash, cart_item_count, quantity_in_cart.

### Do I need to be logged in to e.leclerc?

No. It only uses pages of e.leclerc that are reachable without signing in.

### Does it change anything on e.leclerc, or only read data?

It makes changes on e.leclerc, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/e.leclerc/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/e.leclerc/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/e.leclerc/add_to_cart
