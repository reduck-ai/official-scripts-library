# List the items in the Hot Topic cart

Automatically list the items in the Hot Topic cart on hottopic.com. List the items in the Hot Topic (hottopic.com, US) shopping bag of this browser, as the site holds it: for each line its line id, product id, offer id (the size or color), name, seller (always Hot Topic), quantity, unit price and line price in US dollars after the promotions the bag applies, plus the number of units and the estimated subtotal, before shipping and tax. The bag is the guest bag of the browser, so no sign-in is needed. An empty bag returns an empty list, a zero count and a zero total.

- Site: hottopic.com
- Address: `reduck/hottopic.com/list_cart_items`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hottopic.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hottopic.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Number of units in the bag.
- `lines` (array, required)
- `total` (number | null, required): Estimated subtotal in US dollars, before shipping and tax.

## FAQ

### What does "List the items in the Hot Topic cart" do?

List the items in the Hot Topic (hottopic.com, US) shopping bag of this browser, as the site holds it: for each line its line id, product id, offer id (the size or color), name, seller (always Hot Topic), quantity, unit price and line price in US dollars after the promotions the bag applies, plus the number of units and the estimated subtotal, before shipping and tax. The bag is the guest bag of the browser, so no sign-in is needed. An empty bag returns an empty list, a zero count and a zero total.

### How do I automatically list the items in the Hot Topic cart on hottopic.com?

Ask an AI agent connected to Reduck to run reduck/hottopic.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hottopic.com/list_cart_items

### Is there a hottopic.com API to list the items in the Hot Topic cart?

You do not need one. "List the items in the Hot Topic cart" drives the real hottopic.com pages in a browser, so it works whether or not hottopic.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to hottopic.com?

No. It only uses pages of hottopic.com that are reachable without signing in.

### Does it change anything on hottopic.com, or only read data?

It only reads. It looks things up on hottopic.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hottopic.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hottopic.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/hottopic.com/list_cart_items
