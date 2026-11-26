# Remove from MediaMarkt Spain cart

Automatically remove from MediaMarkt Spain cart on mediamarkt.es. Remove a product from the guest shopping cart of this browser on MediaMarkt Spain (mediamarkt.es), by product id or product link, whatever its quantity. Returns the cart after the removal and removed true; a product that is not in the cart leaves the cart as it is and returns removed false. Other lines are never touched. No sign-in needed.

- Site: mediamarkt.es
- Address: `reduck/mediamarkt.es/remove_from_cart`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mediamarkt.es/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mediamarkt.es/remove_from_cart
```

## Input

- `product` (string, required): MediaMarkt Spain product id as List MediaMarkt Spain cart items gives it (productId), or the product link.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, required): Cart total in euros, VAT included, before any shipping cost.
- `removed` (boolean, required): True when the product was in the cart and is now gone.

## FAQ

### What does "Remove from MediaMarkt Spain cart" do?

Remove a product from the guest shopping cart of this browser on MediaMarkt Spain (mediamarkt.es), by product id or product link, whatever its quantity. Returns the cart after the removal and removed true; a product that is not in the cart leaves the cart as it is and returns removed false. Other lines are never touched. No sign-in needed.

### How do I automatically remove from MediaMarkt Spain cart on mediamarkt.es?

Ask an AI agent connected to Reduck to run reduck/mediamarkt.es/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mediamarkt.es/remove_from_cart

### Is there a mediamarkt.es API to remove from MediaMarkt Spain cart?

You do not need one. "Remove from MediaMarkt Spain cart" drives the real mediamarkt.es pages in a browser, so it works whether or not mediamarkt.es offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to mediamarkt.es?

No. It only uses pages of mediamarkt.es that are reachable without signing in.

### Does it change anything on mediamarkt.es, or only read data?

It makes changes on mediamarkt.es, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mediamarkt.es/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mediamarkt.es/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/mediamarkt.es/remove_from_cart
