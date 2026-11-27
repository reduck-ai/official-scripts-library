# List Mercado Livre cart items

Automatically list Mercado Livre cart items on mercadolibre.com. List the items in your Mercado Livre Brazil (mercadolivre.com.br) cart: for each line its listing id, catalog product id, name, quantity, unit price and line price, plus the item count and total in BRL. An empty cart returns count 0 and an empty list.

- Site: mercadolibre.com
- Address: `reduck/mercadolibre.com/list_cart_items`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mercadolibre.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mercadolibre.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, required): Cart total in BRL as the cart summary shows it.

## FAQ

### What does "List Mercado Livre cart items" do?

List the items in your Mercado Livre Brazil (mercadolivre.com.br) cart: for each line its listing id, catalog product id, name, quantity, unit price and line price, plus the item count and total in BRL. An empty cart returns count 0 and an empty list.

### How do I automatically list Mercado Livre cart items on mercadolibre.com?

Ask an AI agent connected to Reduck to run reduck/mercadolibre.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mercadolibre.com/list_cart_items

### Is there a mercadolibre.com API to list Mercado Livre cart items?

You do not need one. "List Mercado Livre cart items" drives the real mercadolibre.com pages in a browser, so it works whether or not mercadolibre.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to mercadolibre.com?

Yes. It acts as you on mercadolibre.com: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for mercadolibre.com.

### Does it change anything on mercadolibre.com, or only read data?

It only reads. It looks things up on mercadolibre.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mercadolibre.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mercadolibre.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/mercadolibre.com/list_cart_items
