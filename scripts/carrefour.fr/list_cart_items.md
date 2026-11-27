# List Carrefour cart items

Automatically list Carrefour cart items on carrefour.fr. List the items in the Carrefour.fr cart of this browser (guest or signed in): grocery, home-delivered and marketplace lines, each with its line id, barcode number, offer id, name, seller, quantity, unit price and line price in euros and its review_hash (pass it to Remove Carrefour product from cart), plus the item count and total. An empty cart returns an empty list.

- Site: carrefour.fr
- Address: `reduck/carrefour.fr/list_cart_items`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/carrefour.fr/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/carrefour.fr/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number, required)

## FAQ

### What does "List Carrefour cart items" do?

List the items in the Carrefour.fr cart of this browser (guest or signed in): grocery, home-delivered and marketplace lines, each with its line id, barcode number, offer id, name, seller, quantity, unit price and line price in euros and its review_hash (pass it to Remove Carrefour product from cart), plus the item count and total. An empty cart returns an empty list.

### How do I automatically list Carrefour cart items on carrefour.fr?

Ask an AI agent connected to Reduck to run reduck/carrefour.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/carrefour.fr/list_cart_items

### Is there a carrefour.fr API to list Carrefour cart items?

You do not need one. "List Carrefour cart items" drives the real carrefour.fr pages in a browser, so it works whether or not carrefour.fr offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to carrefour.fr?

No. It only uses pages of carrefour.fr that are reachable without signing in.

### Does it change anything on carrefour.fr, or only read data?

It only reads. It looks things up on carrefour.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/carrefour.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/carrefour.fr/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/carrefour.fr/list_cart_items
