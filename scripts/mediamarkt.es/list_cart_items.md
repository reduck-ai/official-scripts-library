# List MediaMarkt Spain cart items

Automatically list MediaMarkt Spain cart items on mediamarkt.es. Read the guest shopping cart of this browser on MediaMarkt Spain (mediamarkt.es): number of articles, total in euros and every line with its product id, name, seller, quantity, unit price and line price. An empty cart returns count 0 and no lines. No sign-in needed.

- Site: mediamarkt.es
- Address: `reduck/mediamarkt.es/list_cart_items`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mediamarkt.es/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mediamarkt.es/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Number of articles in the cart, quantities included.
- `lines` (array, required)
- `total` (number | null, required): Cart total in euros, VAT included, before any shipping cost.

## FAQ

### What does "List MediaMarkt Spain cart items" do?

Read the guest shopping cart of this browser on MediaMarkt Spain (mediamarkt.es): number of articles, total in euros and every line with its product id, name, seller, quantity, unit price and line price. An empty cart returns count 0 and no lines. No sign-in needed.

### How do I automatically list MediaMarkt Spain cart items on mediamarkt.es?

Ask an AI agent connected to Reduck to run reduck/mediamarkt.es/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mediamarkt.es/list_cart_items

### Is there a mediamarkt.es API to list MediaMarkt Spain cart items?

You do not need one. "List MediaMarkt Spain cart items" drives the real mediamarkt.es pages in a browser, so it works whether or not mediamarkt.es offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to mediamarkt.es?

No. It only uses pages of mediamarkt.es that are reachable without signing in.

### Does it change anything on mediamarkt.es, or only read data?

It only reads. It looks things up on mediamarkt.es and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mediamarkt.es/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mediamarkt.es/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/mediamarkt.es/list_cart_items
