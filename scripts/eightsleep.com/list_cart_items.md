# List Eight Sleep cart items

Automatically list Eight Sleep cart items on eightsleep.com. List the lines of the Eight Sleep US guest cart in this browser: each line's id, product id, offer id, name, seller, quantity, unit price and line price, plus the item count and the cart total before tax, in US dollars. A browser with no cart gives an empty list and a total of 0. Pass a line id to eightsleep.com/remove_from_cart.

- Site: eightsleep.com
- Address: `reduck/eightsleep.com/list_cart_items`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/eightsleep.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/eightsleep.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Number of items in the cart: the sum of the line quantities.
- `lines` (array, required)
- `total` (number, required): Cart total before tax, in US dollars.

## FAQ

### What does "List Eight Sleep cart items" do?

List the lines of the Eight Sleep US guest cart in this browser: each line's id, product id, offer id, name, seller, quantity, unit price and line price, plus the item count and the cart total before tax, in US dollars. A browser with no cart gives an empty list and a total of 0. Pass a line id to eightsleep.com/remove_from_cart.

### How do I automatically list Eight Sleep cart items on eightsleep.com?

Ask an AI agent connected to Reduck to run reduck/eightsleep.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/eightsleep.com/list_cart_items

### Is there a eightsleep.com API to list Eight Sleep cart items?

You do not need one. "List Eight Sleep cart items" drives the real eightsleep.com pages in a browser, so it works whether or not eightsleep.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to eightsleep.com?

No. It only uses pages of eightsleep.com that are reachable without signing in.

### Does it change anything on eightsleep.com, or only read data?

It only reads. It looks things up on eightsleep.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/eightsleep.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/eightsleep.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/eightsleep.com/list_cart_items
