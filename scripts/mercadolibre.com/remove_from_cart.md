# Remove from Mercado Livre cart

Automatically remove from Mercado Livre cart on mercadolibre.com. Remove a listing from your Mercado Livre Brazil (mercadolivre.com.br) cart, whatever its quantity, and return the cart after. A listing not in the cart returns removed false and changes nothing.

- Site: mercadolibre.com
- Address: `reduck/mercadolibre.com/remove_from_cart`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mercadolibre.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mercadolibre.com/remove_from_cart
```

## Input

- `item` (string, required): The listing id (MLB4471841974, as list_cart_items returns in offerId) or a Mercado Livre link carrying it.

## Output

- `cart` (object, required)
- `removed` (boolean, required)

## FAQ

### What does "Remove from Mercado Livre cart" do?

Remove a listing from your Mercado Livre Brazil (mercadolivre.com.br) cart, whatever its quantity, and return the cart after. A listing not in the cart returns removed false and changes nothing.

### How do I automatically remove from Mercado Livre cart on mercadolibre.com?

Ask an AI agent connected to Reduck to run reduck/mercadolibre.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mercadolibre.com/remove_from_cart

### Is there a mercadolibre.com API to remove from Mercado Livre cart?

You do not need one. "Remove from Mercado Livre cart" drives the real mercadolibre.com pages in a browser, so it works whether or not mercadolibre.com offers an API for this.

### What information do I need to provide?

Required: item.

### What does it return?

It returns cart, removed.

### Do I need to be logged in to mercadolibre.com?

Yes. It acts as you on mercadolibre.com: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for mercadolibre.com.

### Does it change anything on mercadolibre.com, or only read data?

It makes changes on mercadolibre.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mercadolibre.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mercadolibre.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/mercadolibre.com/remove_from_cart
