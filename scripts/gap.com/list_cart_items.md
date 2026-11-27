# List the items in the Gap cart

Automatically list the items in the Gap cart on gap.com. List the items in the Gap US (gap.com) shopping bag of this browser, as the site holds it. For each line: its line id (to pass to Remove a product from the Gap cart), product id, offer id (the sku), name, seller, quantity, unit price and line price in US dollars after the offers Gap applies in the bag. Gap can show units of one size on several lines, for example when an offer prices them differently. Also returns the number of units and the estimated total, before tax and shipping. The bag is the guest bag of the browser, so no sign-in is needed. An empty bag returns an empty list and a zero count.

- Site: gap.com
- Address: `reduck/gap.com/list_cart_items`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/gap.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/gap.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, required)

## FAQ

### What does "List the items in the Gap cart" do?

List the items in the Gap US (gap.com) shopping bag of this browser, as the site holds it. For each line: its line id (to pass to Remove a product from the Gap cart), product id, offer id (the sku), name, seller, quantity, unit price and line price in US dollars after the offers Gap applies in the bag. Gap can show units of one size on several lines, for example when an offer prices them differently. Also returns the number of units and the estimated total, before tax and shipping. The bag is the guest bag of the browser, so no sign-in is needed. An empty bag returns an empty list and a zero count.

### How do I automatically list the items in the Gap cart on gap.com?

Ask an AI agent connected to Reduck to run reduck/gap.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gap.com/list_cart_items

### Is there a gap.com API to list the items in the Gap cart?

You do not need one. "List the items in the Gap cart" drives the real gap.com pages in a browser, so it works whether or not gap.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to gap.com?

No. It only uses pages of gap.com that are reachable without signing in.

### Does it change anything on gap.com, or only read data?

It only reads. It looks things up on gap.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/gap.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gap.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/gap.com/list_cart_items
