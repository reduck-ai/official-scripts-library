# List Back Market France cart items

Automatically list Back Market France cart items on backmarket.fr. List the items in the backmarket.fr cart of this browser, as the site holds it: for each line its product id, offer id, name, seller, condition grade, quantity, unit price and line price in euros, plus the number of items and the cart total. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list and a zero count.

- Site: backmarket.fr
- Address: `reduck/backmarket.fr/list_cart_items`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/backmarket.fr/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/backmarket.fr/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, optional)

## FAQ

### What does "List Back Market France cart items" do?

List the items in the backmarket.fr cart of this browser, as the site holds it: for each line its product id, offer id, name, seller, condition grade, quantity, unit price and line price in euros, plus the number of items and the cart total. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list and a zero count.

### How do I automatically list Back Market France cart items on backmarket.fr?

Ask an AI agent connected to Reduck to run reduck/backmarket.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/backmarket.fr/list_cart_items

### Is there a backmarket.fr API to list Back Market France cart items?

You do not need one. "List Back Market France cart items" drives the real backmarket.fr pages in a browser, so it works whether or not backmarket.fr offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to backmarket.fr?

No. It only uses pages of backmarket.fr that are reachable without signing in.

### Does it change anything on backmarket.fr, or only read data?

It only reads. It looks things up on backmarket.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/backmarket.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/backmarket.fr/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/backmarket.fr/list_cart_items
