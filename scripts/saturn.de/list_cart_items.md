# List SATURN cart items

Automatically list SATURN cart items on saturn.de. Read the guest shopping cart of this browser on SATURN Germany (saturn.de, the German store): number of articles, total and currency, and every line with its line id, product id, Marketplace offer id, name, seller (SATURN or the Marketplace seller), quantity, unit price and line price in euros. An empty cart returns count 0 and no lines. No sign-in needed.

- Site: saturn.de
- Address: `reduck/saturn.de/list_cart_items`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/saturn.de/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/saturn.de/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Number of articles in the cart, quantities included.
- `lines` (array, required): SATURN lines first, then Marketplace lines by seller, as the cart page shows them.
- `total` (number | null, required): Cart total, VAT included, before any shipping cost the checkout adds.
- `currency` (string | null, required): Currency of the prices, EUR.

## FAQ

### What does "List SATURN cart items" do?

Read the guest shopping cart of this browser on SATURN Germany (saturn.de, the German store): number of articles, total and currency, and every line with its line id, product id, Marketplace offer id, name, seller (SATURN or the Marketplace seller), quantity, unit price and line price in euros. An empty cart returns count 0 and no lines. No sign-in needed.

### How do I automatically list SATURN cart items on saturn.de?

Ask an AI agent connected to Reduck to run reduck/saturn.de/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/saturn.de/list_cart_items

### Is there a saturn.de API to list SATURN cart items?

You do not need one. "List SATURN cart items" drives the real saturn.de pages in a browser, so it works whether or not saturn.de offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total, currency.

### Do I need to be logged in to saturn.de?

No. It only uses pages of saturn.de that are reachable without signing in.

### Does it change anything on saturn.de, or only read data?

It only reads. It looks things up on saturn.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/saturn.de/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/saturn.de/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/saturn.de/list_cart_items
