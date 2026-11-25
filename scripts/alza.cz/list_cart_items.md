# List Alza.cz cart items

Automatically list Alza.cz cart items on alza.cz. List what is in the Alza.cz shopping cart of this browser: each line with its product id, name, quantity, unit price and line price in Czech crowns, plus the item count and the total to pay with taxes. Works as a guest, with no account: the cart lives in the browser. An empty cart returns no lines and a count of zero. Nothing is paid or ordered.

- Site: alza.cz
- Address: `reduck/alza.cz/list_cart_items`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/alza.cz/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/alza.cz/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Units in the cart.
- `lines` (array, required)
- `total` (number | null, required): Cart total in Czech crowns, taxes included. Null when the cart is empty.

## FAQ

### What does "List Alza.cz cart items" do?

List what is in the Alza.cz shopping cart of this browser: each line with its product id, name, quantity, unit price and line price in Czech crowns, plus the item count and the total to pay with taxes. Works as a guest, with no account: the cart lives in the browser. An empty cart returns no lines and a count of zero. Nothing is paid or ordered.

### How do I automatically list Alza.cz cart items on alza.cz?

Ask an AI agent connected to Reduck to run reduck/alza.cz/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/alza.cz/list_cart_items

### Is there a alza.cz API to list Alza.cz cart items?

You do not need one. "List Alza.cz cart items" drives the real alza.cz pages in a browser, so it works whether or not alza.cz offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to alza.cz?

No. It only uses pages of alza.cz that are reachable without signing in.

### Does it change anything on alza.cz, or only read data?

It only reads. It looks things up on alza.cz and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/alza.cz/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/alza.cz/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/alza.cz/list_cart_items
