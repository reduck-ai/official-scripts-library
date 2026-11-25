# List IKEA France cart items

Automatically list IKEA France cart items on ikea.com. List the items in the IKEA France (ikea.com/fr/fr) cart of this browser, as the site holds it: for each line its article number, name, quantity, unit price and line price in euros, plus the number of items and the cart total. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list and a zero count.

- Site: ikea.com
- Address: `reduck/ikea.com/list_cart_items`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ikea.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ikea.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, optional)

## FAQ

### What does "List IKEA France cart items" do?

List the items in the IKEA France (ikea.com/fr/fr) cart of this browser, as the site holds it: for each line its article number, name, quantity, unit price and line price in euros, plus the number of items and the cart total. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list and a zero count.

### How do I automatically list IKEA France cart items on ikea.com?

Ask an AI agent connected to Reduck to run reduck/ikea.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ikea.com/list_cart_items

### Is there a ikea.com API to list IKEA France cart items?

You do not need one. "List IKEA France cart items" drives the real ikea.com pages in a browser, so it works whether or not ikea.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to ikea.com?

No. It only uses pages of ikea.com that are reachable without signing in.

### Does it change anything on ikea.com, or only read data?

It only reads. It looks things up on ikea.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ikea.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ikea.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/ikea.com/list_cart_items
