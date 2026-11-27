# List the items in the HP cart

Automatically list the items in the HP cart on hp.com. List the items in the HP US store (hp.com/us-en/shop) cart of this browser, as the site holds it: for each line its line id, product id (the HP part number), offer id (always null), name, seller (always HP), quantity, unit price and line price in US dollars, plus the number of items and the products total, before tax and shipping. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list and a zero count.

- Site: hp.com
- Address: `reduck/hp.com/list_cart_items`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hp.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hp.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Number of units in the cart, all lines together.
- `lines` (array, required)
- `total` (number | null, required): Total of the products in US dollars, before tax and shipping.

## FAQ

### What does "List the items in the HP cart" do?

List the items in the HP US store (hp.com/us-en/shop) cart of this browser, as the site holds it: for each line its line id, product id (the HP part number), offer id (always null), name, seller (always HP), quantity, unit price and line price in US dollars, plus the number of items and the products total, before tax and shipping. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list and a zero count.

### How do I automatically list the items in the HP cart on hp.com?

Ask an AI agent connected to Reduck to run reduck/hp.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hp.com/list_cart_items

### Is there a hp.com API to list the items in the HP cart?

You do not need one. "List the items in the HP cart" drives the real hp.com pages in a browser, so it works whether or not hp.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to hp.com?

No. It only uses pages of hp.com that are reachable without signing in.

### Does it change anything on hp.com, or only read data?

It only reads. It looks things up on hp.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hp.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hp.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/hp.com/list_cart_items
