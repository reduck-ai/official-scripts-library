# Get Mercado Livre product offers

Automatically get Mercado Livre product offers on mercadolibre.com. List every seller's offer for one Mercado Livre Brazil (mercadolivre.com.br) catalog product, from a listing id or product link: listing id, seller, price, list price and the offer's text lines (condition, delivery, stock) as shown. A listing outside the catalog has one offer, itself.

- Site: mercadolibre.com
- Address: `reduck/mercadolibre.com/get-product-offers`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mercadolibre.com/get-product-offers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mercadolibre.com/get-product-offers
```

## Input

- `item` (string, required): A listing id (MLB4471841974) or a mercadolivre.com.br product link (/p/MLB32489332 or produto.mercadolivre.com.br/MLB-…).

## Output

- `name` (string | null, required)
- `count` (integer, required)
- `offers` (array, required)
- `productId` (string | null, required): Catalog product id (MLB… of /p/), null for a listing outside the catalog.

## FAQ

### What does "Get Mercado Livre product offers" do?

List every seller's offer for one Mercado Livre Brazil (mercadolivre.com.br) catalog product, from a listing id or product link: listing id, seller, price, list price and the offer's text lines (condition, delivery, stock) as shown. A listing outside the catalog has one offer, itself.

### How do I automatically get Mercado Livre product offers on mercadolibre.com?

Ask an AI agent connected to Reduck to run reduck/mercadolibre.com/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mercadolibre.com/get-product-offers

### Is there a mercadolibre.com API to get Mercado Livre product offers?

You do not need one. "Get Mercado Livre product offers" drives the real mercadolibre.com pages in a browser, so it works whether or not mercadolibre.com offers an API for this.

### What information do I need to provide?

Required: item.

### What does it return?

It returns name, count, offers, productId.

### Do I need to be logged in to mercadolibre.com?

Yes. It acts as you on mercadolibre.com: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for mercadolibre.com.

### Does it change anything on mercadolibre.com, or only read data?

It only reads. It looks things up on mercadolibre.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mercadolibre.com/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mercadolibre.com/get-product-offers

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/mercadolibre.com/get-product-offers
