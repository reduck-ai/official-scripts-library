# Add Etsy listing to cart

Automatically add Etsy listing to cart on etsy.com. Add an Etsy (etsy.com) listing to your cart by listing id, with an optional quantity, as a guest or signed in. A listing with option menus (size, color...) needs one choice per menu in options; a missing or wrong choice fails with the menus and their options. Returns the listing's cart line after the add (variation, quantity, unit price, line total, shop), the cart's item count and totals. A sold-out or removed listing fails with a message that says so. Listings that need personalization text are not supported. Never checks out.

- Site: etsy.com
- Address: `reduck/etsy.com/add_to_cart`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/etsy.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/etsy.com/add_to_cart
```

## Input

- `product` (string, required): Etsy listing id (e.g. 4571868333) or listing link (https://www.etsy.com/listing/...), as search-products returns it.
- `options` (array, optional): For a listing with option menus (size, color...), one choice per menu, in the page's order: the option's label as Etsy shows it (e.g. "Large") or its id. Leave out for a listing without options. A wrong or missing choice fails with the menus and their options.
- `quantity` (integer, optional): Number of units to add, 1 to 10.

## Output

- `name` (string | null, required)
- `added` (integer, required): Units this run added.
- `count` (integer, required): Total quantity in the cart.
- `lines` (array, required)
- `total` (number | null, required): Cart total Etsy shows, items and estimated shipping, in the browser's currency.
- `productId` (string, required): Etsy listing id added.
- `offerId` (string | null, optional): The listing's inventory id for the chosen options.

## FAQ

### What does "Add Etsy listing to cart" do?

Add an Etsy (etsy.com) listing to your cart by listing id, with an optional quantity, as a guest or signed in. A listing with option menus (size, color...) needs one choice per menu in options; a missing or wrong choice fails with the menus and their options. Returns the listing's cart line after the add (variation, quantity, unit price, line total, shop), the cart's item count and totals. A sold-out or removed listing fails with a message that says so. Listings that need personalization text are not supported. Never checks out.

### How do I automatically add Etsy listing to cart on etsy.com?

Ask an AI agent connected to Reduck to run reduck/etsy.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/etsy.com/add_to_cart

### Is there a etsy.com API to add Etsy listing to cart?

You do not need one. "Add Etsy listing to cart" drives the real etsy.com pages in a browser, so it works whether or not etsy.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: options, quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to etsy.com?

No. It only uses pages of etsy.com that are reachable without signing in.

### Does it change anything on etsy.com, or only read data?

It makes changes on etsy.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/etsy.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/etsy.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/etsy.com/add_to_cart
