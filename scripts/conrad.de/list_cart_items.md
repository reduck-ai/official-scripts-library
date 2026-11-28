# List Conrad cart items

Automatically list Conrad cart items on conrad.de. List the shopping cart of this browser on Conrad Germany (conrad.de, the German store): each line with its line id, Conrad product id, offer id, name, seller, quantity, unit price and line price, plus the item count, the items total (delivery not included), the currency (euros) and whether the prices include VAT. A browser with no account sees the business customer store, so prices are net prices without VAT. Works as a guest, with no account. A browser that never had a cart gives an empty cart.

- Site: conrad.de
- Address: `reduck/conrad.de/list_cart_items`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/conrad.de/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/conrad.de/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Units in the cart.
- `lines` (array, required)
- `total` (number | null, required): Total of the items in the cart, delivery not included.
- `currency` (string | null, required)
- `pricesIncludeVat` (boolean | null, required): False when the cart shows net prices without VAT. Null for an empty cart of a browser that never had one.

## FAQ

### What does "List Conrad cart items" do?

List the shopping cart of this browser on Conrad Germany (conrad.de, the German store): each line with its line id, Conrad product id, offer id, name, seller, quantity, unit price and line price, plus the item count, the items total (delivery not included), the currency (euros) and whether the prices include VAT. A browser with no account sees the business customer store, so prices are net prices without VAT. Works as a guest, with no account. A browser that never had a cart gives an empty cart.

### How do I automatically list Conrad cart items on conrad.de?

Ask an AI agent connected to Reduck to run reduck/conrad.de/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/conrad.de/list_cart_items

### Is there a conrad.de API to list Conrad cart items?

You do not need one. "List Conrad cart items" drives the real conrad.de pages in a browser, so it works whether or not conrad.de offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total, currency, pricesIncludeVat.

### Do I need to be logged in to conrad.de?

No. It only uses pages of conrad.de that are reachable without signing in.

### Does it change anything on conrad.de, or only read data?

It only reads. It looks things up on conrad.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/conrad.de/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/conrad.de/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/conrad.de/list_cart_items
