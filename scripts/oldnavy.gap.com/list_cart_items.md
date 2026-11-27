# List the items in the Old Navy cart

Automatically list the items in the Old Navy cart on oldnavy.gap.com. List the items in the Old Navy US (oldnavy.gap.com) shopping bag of this browser, as the site holds it. For each line: its line id (to pass to Remove a product from the Old Navy cart), product id, offer id (the sku), name, seller, quantity, unit price and line price in US dollars after the offers Old Navy applies in the bag. Old Navy can show units of one size on several lines, for example when an offer prices them differently. Also returns the number of units and the estimated total, before tax and shipping. The bag is the guest bag of the browser, so no sign-in is needed. An empty bag returns an empty list and a zero count.

- Site: oldnavy.gap.com
- Address: `reduck/oldnavy.gap.com/list_cart_items`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/oldnavy.gap.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/oldnavy.gap.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, required)

## FAQ

### What does "List the items in the Old Navy cart" do?

List the items in the Old Navy US (oldnavy.gap.com) shopping bag of this browser, as the site holds it. For each line: its line id (to pass to Remove a product from the Old Navy cart), product id, offer id (the sku), name, seller, quantity, unit price and line price in US dollars after the offers Old Navy applies in the bag. Old Navy can show units of one size on several lines, for example when an offer prices them differently. Also returns the number of units and the estimated total, before tax and shipping. The bag is the guest bag of the browser, so no sign-in is needed. An empty bag returns an empty list and a zero count.

### How do I automatically list the items in the Old Navy cart on oldnavy.gap.com?

Ask an AI agent connected to Reduck to run reduck/oldnavy.gap.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/oldnavy.gap.com/list_cart_items

### Is there a oldnavy.gap.com API to list the items in the Old Navy cart?

You do not need one. "List the items in the Old Navy cart" drives the real oldnavy.gap.com pages in a browser, so it works whether or not oldnavy.gap.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to oldnavy.gap.com?

No. It only uses pages of oldnavy.gap.com that are reachable without signing in.

### Does it change anything on oldnavy.gap.com, or only read data?

It only reads. It looks things up on oldnavy.gap.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/oldnavy.gap.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/oldnavy.gap.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/oldnavy.gap.com/list_cart_items
