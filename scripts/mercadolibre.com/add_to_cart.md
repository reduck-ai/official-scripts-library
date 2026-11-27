# Add to Mercado Livre cart

Automatically add to Mercado Livre cart on mercadolibre.com. Add 1 to 10 units of a Mercado Livre Brazil (mercadolivre.com.br) listing to your cart, from its listing id or link, and return the cart after the add. Never buys: it uses only the add-to-cart button. A link that is not a product page, or a listing without that stock, is refused with a clear message.

- Site: mercadolibre.com
- Address: `reduck/mercadolibre.com/add_to_cart`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mercadolibre.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mercadolibre.com/add_to_cart
```

## Input

- `item` (string, required): Listing id (MLB4471841974), as search-products / get-product-offers return, or a mercadolivre.com.br product link (/p/MLB…?pdp_filters=item_id:MLB… picks that seller's listing).
- `quantity` (integer, optional)

## Output

- `cart` (object, required)
- `item` (string, required): The listing id that was added.
- `added` (integer, required): Units added by this run.

## FAQ

### What does "Add to Mercado Livre cart" do?

Add 1 to 10 units of a Mercado Livre Brazil (mercadolivre.com.br) listing to your cart, from its listing id or link, and return the cart after the add. Never buys: it uses only the add-to-cart button. A link that is not a product page, or a listing without that stock, is refused with a clear message.

### How do I automatically add to Mercado Livre cart on mercadolibre.com?

Ask an AI agent connected to Reduck to run reduck/mercadolibre.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mercadolibre.com/add_to_cart

### Is there a mercadolibre.com API to add to Mercado Livre cart?

You do not need one. "Add to Mercado Livre cart" drives the real mercadolibre.com pages in a browser, so it works whether or not mercadolibre.com offers an API for this.

### What information do I need to provide?

Required: item. Optional: quantity.

### What does it return?

It returns cart, item, added.

### Do I need to be logged in to mercadolibre.com?

Yes. It acts as you on mercadolibre.com: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for mercadolibre.com.

### Does it change anything on mercadolibre.com, or only read data?

It makes changes on mercadolibre.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mercadolibre.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mercadolibre.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/mercadolibre.com/add_to_cart
