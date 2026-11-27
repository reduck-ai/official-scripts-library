# Get Mercado Livre product

Automatically get Mercado Livre product on mercadolibre.com. Get a Mercado Livre Brazil (mercadolivre.com.br) product from its listing id or link: name, listing and catalog ids, price, list price, condition, seller, stock, images, rating, the number of other offers, and its specifications.

- Site: mercadolibre.com
- Address: `reduck/mercadolibre.com/get-product`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mercadolibre.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mercadolibre.com/get-product
```

## Input

- `item` (string, required): A listing id (MLB4471841974) or a mercadolivre.com.br product link (/p/MLB…, produto.mercadolivre.com.br/MLB-…).

## Output

- `url` (string, required)
- `name` (string, required)
- `price` (number | null, required)
- `offerId` (string | null, required): Listing id of the offer shown in the buy box: pass it to add_to_cart. Null when the product has no active offer.
- `currency` (string, required)
- `productId` (string | null, required): Catalog product id (/p/MLB…), null outside the catalog.
- `specs` (object, optional)
- `images` (array, optional)
- `rating` (number | null, optional)
- `seller` (string | null, optional)
- `soldText` (string | null, optional)
- `condition` (string | null, optional)
- `listPrice` (number | null, optional)
- `sellerUrl` (string | null, optional)
- `stockText` (string | null, optional)
- `reviewCount` (integer | null, optional)
- `officialStore` (boolean, optional)
- `otherOffersText` (string | null, optional)

## FAQ

### What does "Get Mercado Livre product" do?

Get a Mercado Livre Brazil (mercadolivre.com.br) product from its listing id or link: name, listing and catalog ids, price, list price, condition, seller, stock, images, rating, the number of other offers, and its specifications.

### How do I automatically get Mercado Livre product on mercadolibre.com?

Ask an AI agent connected to Reduck to run reduck/mercadolibre.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mercadolibre.com/get-product

### Is there a mercadolibre.com API to get Mercado Livre product?

You do not need one. "Get Mercado Livre product" drives the real mercadolibre.com pages in a browser, so it works whether or not mercadolibre.com offers an API for this.

### What information do I need to provide?

Required: item.

### What does it return?

It returns url, name, price, specs, images, rating, seller, offerId, currency, soldText, condition, listPrice, productId, sellerUrl, stockText, reviewCount, officialStore, otherOffersText.

### Do I need to be logged in to mercadolibre.com?

Yes. It acts as you on mercadolibre.com: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for mercadolibre.com.

### Does it change anything on mercadolibre.com, or only read data?

It only reads. It looks things up on mercadolibre.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mercadolibre.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mercadolibre.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/mercadolibre.com/get-product
