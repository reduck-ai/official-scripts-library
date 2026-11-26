# List LDLC cart items

Automatically list LDLC cart items on ldlc.com. List the items in the LDLC cart of this browser, as the site holds it: for each line its product id, offer id, name, quantity, unit price and line price in euros, plus the number of items and the cart total with taxes. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list and a zero count.

- Site: ldlc.com
- Address: `reduck/ldlc.com/list_cart_items`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ldlc.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ldlc.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Units in the cart.
- `lines` (array, required)
- `total` (number | null, required): Cart total in euros, taxes included.

## FAQ

### What does "List LDLC cart items" do?

List the items in the LDLC cart of this browser, as the site holds it: for each line its product id, offer id, name, quantity, unit price and line price in euros, plus the number of items and the cart total with taxes. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list and a zero count.

### How do I automatically list LDLC cart items on ldlc.com?

Ask an AI agent connected to Reduck to run reduck/ldlc.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ldlc.com/list_cart_items

### Is there a ldlc.com API to list LDLC cart items?

You do not need one. "List LDLC cart items" drives the real ldlc.com pages in a browser, so it works whether or not ldlc.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to ldlc.com?

No. It only uses pages of ldlc.com that are reachable without signing in.

### Does it change anything on ldlc.com, or only read data?

It only reads. It looks things up on ldlc.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ldlc.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ldlc.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/ldlc.com/list_cart_items
