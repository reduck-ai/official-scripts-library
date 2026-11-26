# Add eBay item to cart

Automatically add eBay item to cart on ebay.com. Add an eBay (ebay.com) Buy It Now item to your cart by item id, with an optional quantity, as a guest or signed in. For a listing with variations (size, color...), pass variation_id. Returns the item's cart line after the add (title, seller, quantity, unit price, line total, shipping), the cart's item count and subtotal, and whether it is a guest cart. A listing that does not exist, has ended, or sells only by auction fails with a message that says so. Never checks out.

- Site: ebay.com
- Address: `reduck/ebay.com/add_to_cart`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ebay.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ebay.com/add_to_cart
```

## Input

- `product` (string, required): eBay item id (e.g. 366835648867) or listing link (https://www.ebay.com/itm/...), as search-products returns it.
- `quantity` (integer, optional): Number of units to add, 1 to 10.
- `variation_id` (string, optional): For a listing with variations (size, color...), the variation to add: the var value of the listing link (ebay.com/itm/<id>?var=<variation_id>). Leave out otherwise.

## Output

- `name` (string | null, required)
- `added` (integer, required): Units this run added. Lower than quantity when the seller has fewer units left.
- `count` (integer, required): Total quantity in the cart.
- `lines` (array, required)
- `total` (number | null, required): Cart subtotal eBay shows, items and shipping, in the cart currency (USD on ebay.com).
- `productId` (string, required): eBay item id added.
- `offerId` (string | null, optional): Variation added, for a multi-variation listing; null otherwise.

## FAQ

### What does "Add eBay item to cart" do?

Add an eBay (ebay.com) Buy It Now item to your cart by item id, with an optional quantity, as a guest or signed in. For a listing with variations (size, color...), pass variation_id. Returns the item's cart line after the add (title, seller, quantity, unit price, line total, shipping), the cart's item count and subtotal, and whether it is a guest cart. A listing that does not exist, has ended, or sells only by auction fails with a message that says so. Never checks out.

### How do I automatically add eBay item to cart on ebay.com?

Ask an AI agent connected to Reduck to run reduck/ebay.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ebay.com/add_to_cart

### Is there a ebay.com API to add eBay item to cart?

You do not need one. "Add eBay item to cart" drives the real ebay.com pages in a browser, so it works whether or not ebay.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: quantity, variation_id.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to ebay.com?

No. It only uses pages of ebay.com that are reachable without signing in.

### Does it change anything on ebay.com, or only read data?

It makes changes on ebay.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ebay.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ebay.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/ebay.com/add_to_cart
