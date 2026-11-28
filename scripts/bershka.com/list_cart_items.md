# List Bershka cart items

Automatically list Bershka cart items on bershka.com. List the items in the Bershka France (bershka.com/fr) cart of this browser: each line with its line id, product id, offerId (the size), name, colour, size and length, quantity, unit price and line price in euros, plus the number of units and the total of the cart. An empty cart gives an empty list. The cart works without sign-in and stays with the browser.

- Site: bershka.com
- Address: `reduck/bershka.com/list_cart_items`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bershka.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bershka.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Number of units in the cart.
- `lines` (array, required)
- `total` (number | null, required): Total of the cart, in euros.
- `currency` (string, required): Currency of the amounts, as an ISO code (euro).

## FAQ

### What does "List Bershka cart items" do?

List the items in the Bershka France (bershka.com/fr) cart of this browser: each line with its line id, product id, offerId (the size), name, colour, size and length, quantity, unit price and line price in euros, plus the number of units and the total of the cart. An empty cart gives an empty list. The cart works without sign-in and stays with the browser.

### How do I automatically list Bershka cart items on bershka.com?

Ask an AI agent connected to Reduck to run reduck/bershka.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bershka.com/list_cart_items

### Is there a bershka.com API to list Bershka cart items?

You do not need one. "List Bershka cart items" drives the real bershka.com pages in a browser, so it works whether or not bershka.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total, currency.

### Do I need to be logged in to bershka.com?

No. It only uses pages of bershka.com that are reachable without signing in.

### Does it change anything on bershka.com, or only read data?

It only reads. It looks things up on bershka.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bershka.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bershka.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/bershka.com/list_cart_items
