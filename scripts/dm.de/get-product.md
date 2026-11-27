# Get dm product

Automatically get dm product on dm.de. Fetch one dm Germany (dm.de, the German store) product page by product id or product link. Returns title, brand, barcode number, link, price in euros, unit price text, the price note dm shows (for example since when the price did not go up), category path, images, labels, the description sections (description, features, ingredients, use and others), online availability with the quantities the shop lets a person order, the other sizes or colors with their product ids, rating and review count. Prices and availability are what dm shows a new guest with no dm store chosen; availability in one dm store is not part of it. Texts are in German. An unknown product id fails with an error that says so.

- Site: dm.de
- Address: `reduck/dm.de/get-product`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dm.de/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dm.de/get-product
```

## Input

- `product` (string, required): dm product id (the product_id of Search dm products, the number after /p/d/ in a product link), or the product link itself.

## Output

- `url` (string | null, required)
- `price` (number | null, required): Price, VAT included.
- `title` (string | null, required)
- `currency` (string | null, required): Currency of the price, EUR.
- `requested` (string, required): The product argument as given.
- `product_id` (string, required): dm product id (dm article number).
- `gtin` (string | null, optional): EAN (GTIN) barcode.
- `brand` (string | null, optional)
- `images` (array, optional)
- `labels` (array, optional): Short labels dm shows on the product, for example Vegan.
- `rating` (number | null, optional): Average rating out of 5. Null when nobody rated the product.
- `sections` (array, optional): The description sections of the page, each with its heading and its text.
- `variants` (array, optional): The other sizes or colors of the product, each its own product id, this one included. Empty when there are none.
- `breadcrumb` (array, optional): Category path, in German.
- `price_note` (string | null, optional): The note dm shows next to the price, for example since when the price did not go up. Null when none is shown.
- `is_pharmacy` (boolean | null, optional)
- `purchasable` (boolean | null, optional): True when the online shop sells the product now.
- `availability` (array, optional): The availability lines dm shows, as text, for example Lieferbar.
- `review_count` (integer | null, optional)
- `unit_price_text` (string | null, optional): Contents and price per unit as dm shows it.
- `quantity_options` (array, optional): The quantities the shop lets a person pick.

## FAQ

### What does "Get dm product" do?

Fetch one dm Germany (dm.de, the German store) product page by product id or product link. Returns title, brand, barcode number, link, price in euros, unit price text, the price note dm shows (for example since when the price did not go up), category path, images, labels, the description sections (description, features, ingredients, use and others), online availability with the quantities the shop lets a person order, the other sizes or colors with their product ids, rating and review count. Prices and availability are what dm shows a new guest with no dm store chosen; availability in one dm store is not part of it. Texts are in German. An unknown product id fails with an error that says so.

### How do I automatically get dm product on dm.de?

Ask an AI agent connected to Reduck to run reduck/dm.de/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dm.de/get-product

### Is there a dm.de API to get dm product?

You do not need one. "Get dm product" drives the real dm.de pages in a browser, so it works whether or not dm.de offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns url, gtin, brand, price, title, images, labels, rating, currency, sections, variants, requested, breadcrumb, price_note, product_id, is_pharmacy, purchasable, availability, review_count, unit_price_text, quantity_options.

### Do I need to be logged in to dm.de?

No. It only uses pages of dm.de that are reachable without signing in.

### Does it change anything on dm.de, or only read data?

It only reads. It looks things up on dm.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dm.de/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dm.de/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/dm.de/get-product
