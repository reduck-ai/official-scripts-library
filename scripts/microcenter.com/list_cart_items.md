# List the items in the Micro Center cart

Automatically list the items in the Micro Center cart on microcenter.com. List the items in the Micro Center (microcenter.com) cart of this browser, as the site holds it: for each line its line id, product id, offer id (always null), name, seller (always Micro Center), quantity, unit price and line price in US dollars, plus the number of items and the cart total Micro Center shows (before tax, with the shipping price of shippable items). The cart is the guest cart of the browser, so no sign-in is needed. Saved list items are not included. An empty cart returns an empty list and a zero count.

- Site: microcenter.com
- Address: `reduck/microcenter.com/list_cart_items`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/microcenter.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/microcenter.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Number of units in the cart, all lines together.
- `lines` (array, required)
- `total` (number | null, required): Cart total in US dollars as Micro Center shows it, before tax, with the shipping price of shippable items.

## FAQ

### What does "List the items in the Micro Center cart" do?

List the items in the Micro Center (microcenter.com) cart of this browser, as the site holds it: for each line its line id, product id, offer id (always null), name, seller (always Micro Center), quantity, unit price and line price in US dollars, plus the number of items and the cart total Micro Center shows (before tax, with the shipping price of shippable items). The cart is the guest cart of the browser, so no sign-in is needed. Saved list items are not included. An empty cart returns an empty list and a zero count.

### How do I automatically list the items in the Micro Center cart on microcenter.com?

Ask an AI agent connected to Reduck to run reduck/microcenter.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/microcenter.com/list_cart_items

### Is there a microcenter.com API to list the items in the Micro Center cart?

You do not need one. "List the items in the Micro Center cart" drives the real microcenter.com pages in a browser, so it works whether or not microcenter.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to microcenter.com?

No. It only uses pages of microcenter.com that are reachable without signing in.

### Does it change anything on microcenter.com, or only read data?

It only reads. It looks things up on microcenter.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/microcenter.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/microcenter.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/microcenter.com/list_cart_items
