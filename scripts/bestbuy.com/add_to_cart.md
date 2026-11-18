# Add to Best Buy cart

Automatically add to Best Buy cart on bestbuy.com. Add one unit of a Best Buy (US) product to this browser's Best Buy cart, by SKU, with shipping as the delivery method, as the product page's add-to-cart button does. Returns the product's quantity in the cart after the add, the cart's item count and its subtotal. Adding a SKU already in the cart adds one more. A product that cannot be added (sold out, inactive, coming soon) fails with an error that gives Best Buy's state for it. List Best Buy cart items gives the cart with tax and total; Remove from Best Buy cart takes the item out.

- Site: bestbuy.com
- Address: `reduck/bestbuy.com/add_to_cart`
- Updated: 2026-11-17 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bestbuy.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bestbuy.com/add_to_cart
```

## Input

- `sku` (string, required): Best Buy SKU, as Search Best Buy products and Get Best Buy product give it.

## Output

- `sku` (string, required)
- `quantity` (integer, required): Units of this SKU in the cart after the add.
- `cart_subtotal` (number | null, required): Cart subtotal in US dollars, before tax and shipping.
- `cart_item_count` (integer, required)
- `unit_price` (number | null, optional)

## FAQ

### What does "Add to Best Buy cart" do?

Add one unit of a Best Buy (US) product to this browser's Best Buy cart, by SKU, with shipping as the delivery method, as the product page's add-to-cart button does. Returns the product's quantity in the cart after the add, the cart's item count and its subtotal. Adding a SKU already in the cart adds one more. A product that cannot be added (sold out, inactive, coming soon) fails with an error that gives Best Buy's state for it. List Best Buy cart items gives the cart with tax and total; Remove from Best Buy cart takes the item out.

### How do I automatically add to Best Buy cart on bestbuy.com?

Ask an AI agent connected to Reduck to run reduck/bestbuy.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bestbuy.com/add_to_cart

### Is there a bestbuy.com API to add to Best Buy cart?

You do not need one. "Add to Best Buy cart" drives the real bestbuy.com pages in a browser, so it works whether or not bestbuy.com offers an API for this.

### What information do I need to provide?

Required: sku.

### What does it return?

It returns sku, quantity, unit_price, cart_subtotal, cart_item_count.

### Do I need to be logged in to bestbuy.com?

No. It only uses pages of bestbuy.com that are reachable without signing in.

### Does it change anything on bestbuy.com, or only read data?

It makes changes on bestbuy.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bestbuy.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bestbuy.com/add_to_cart

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/bestbuy.com/add_to_cart
