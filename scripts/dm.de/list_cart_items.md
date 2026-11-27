# List dm cart items

Automatically list dm cart items on dm.de. Read the guest shopping cart of this browser on dm Germany (dm.de, the German store): number of articles, value of the articles and currency, and every line with its product id, name, seller (dm), quantity, unit price and line price in euros. The total is the value of the articles before the shipping cost that the checkout adds. Prices are the online shop prices dm shows a new guest with no dm store chosen. An empty cart returns count 0 and no lines. No sign-in needed.

- Site: dm.de
- Address: `reduck/dm.de/list_cart_items`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dm.de/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dm.de/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Number of articles in the cart, quantities included.
- `lines` (array, required)
- `total` (number | null, required): Value of the articles, VAT included, before the shipping cost the checkout adds.
- `currency` (string | null, required): Currency of the prices, EUR. Null for an empty cart, for which dm gives none.

## FAQ

### What does "List dm cart items" do?

Read the guest shopping cart of this browser on dm Germany (dm.de, the German store): number of articles, value of the articles and currency, and every line with its product id, name, seller (dm), quantity, unit price and line price in euros. The total is the value of the articles before the shipping cost that the checkout adds. Prices are the online shop prices dm shows a new guest with no dm store chosen. An empty cart returns count 0 and no lines. No sign-in needed.

### How do I automatically list dm cart items on dm.de?

Ask an AI agent connected to Reduck to run reduck/dm.de/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dm.de/list_cart_items

### Is there a dm.de API to list dm cart items?

You do not need one. "List dm cart items" drives the real dm.de pages in a browser, so it works whether or not dm.de offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total, currency.

### Do I need to be logged in to dm.de?

No. It only uses pages of dm.de that are reachable without signing in.

### Does it change anything on dm.de, or only read data?

It only reads. It looks things up on dm.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dm.de/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dm.de/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/dm.de/list_cart_items
