# List the Fnac cart items

Automatically list the Fnac cart items on fnac.com. List the items in the Fnac.com cart of this browser, as the site holds it: for each line its product id, offer id, name, seller (Fnac itself or the marketplace seller), quantity, unit price and line price in euros, plus the number of items and the cart total. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list and a zero count.

- Site: fnac.com
- Address: `reduck/fnac.com/list_cart_items`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/fnac.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/fnac.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Number of items in the cart, quantities summed.
- `lines` (array, required)
- `total` (number | null, required): Cart total in euros as the site states it.

## FAQ

### What does "List the Fnac cart items" do?

List the items in the Fnac.com cart of this browser, as the site holds it: for each line its product id, offer id, name, seller (Fnac itself or the marketplace seller), quantity, unit price and line price in euros, plus the number of items and the cart total. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list and a zero count.

### How do I automatically list the Fnac cart items on fnac.com?

Ask an AI agent connected to Reduck to run reduck/fnac.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/fnac.com/list_cart_items

### Is there a fnac.com API to list the Fnac cart items?

You do not need one. "List the Fnac cart items" drives the real fnac.com pages in a browser, so it works whether or not fnac.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to fnac.com?

No. It only uses pages of fnac.com that are reachable without signing in.

### Does it change anything on fnac.com, or only read data?

It only reads. It looks things up on fnac.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/fnac.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/fnac.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/fnac.com/list_cart_items
