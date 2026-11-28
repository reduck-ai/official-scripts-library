# List Alternate cart items

Automatically list Alternate cart items on alternate.de. List the shopping cart of this browser on Alternate Germany (alternate.de, the German store): each line with its product id (also its line id), name, quantity, unit price and line price in euros (VAT included), plus the item count, the items total (delivery not included) and the currency. Alternate sells every product itself, so offerId and seller are null. Works as a guest, with no account. A browser that never had a cart gives an empty cart.

- Site: alternate.de
- Address: `reduck/alternate.de/list_cart_items`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/alternate.de/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/alternate.de/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Units in the cart.
- `lines` (array, required)
- `total` (number | null, required): Total of the item lines in euros, VAT included, delivery not included.
- `currency` (string, required)

## FAQ

### What does "List Alternate cart items" do?

List the shopping cart of this browser on Alternate Germany (alternate.de, the German store): each line with its product id (also its line id), name, quantity, unit price and line price in euros (VAT included), plus the item count, the items total (delivery not included) and the currency. Alternate sells every product itself, so offerId and seller are null. Works as a guest, with no account. A browser that never had a cart gives an empty cart.

### How do I automatically list Alternate cart items on alternate.de?

Ask an AI agent connected to Reduck to run reduck/alternate.de/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/alternate.de/list_cart_items

### Is there a alternate.de API to list Alternate cart items?

You do not need one. "List Alternate cart items" drives the real alternate.de pages in a browser, so it works whether or not alternate.de offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total, currency.

### Do I need to be logged in to alternate.de?

No. It only uses pages of alternate.de that are reachable without signing in.

### Does it change anything on alternate.de, or only read data?

It only reads. It looks things up on alternate.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/alternate.de/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/alternate.de/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/alternate.de/list_cart_items
