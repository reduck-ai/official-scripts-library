# Get AliExpress product

Automatically get AliExpress product on aliexpress.com. Fetch one AliExpress product from its id or its product page link (as returned by Search AliExpress products). Returns the title, the price and currency of the variant the page selects, availability, rating, review count, sold-count text, images, category, the seller (store name, store id, seller id, positive feedback rate, country) and every variant with its sku id (the id that Add AliExpress product to cart takes), options, price, stock and whether it can be bought. Prices and texts follow the AliExpress site and currency of the browser. An unknown product, or a product AliExpress does not sell in the browser's region, fails with an error that says so; a link that is not a product page fails too.

- Site: aliexpress.com
- Address: `reduck/aliexpress.com/get-product`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/aliexpress.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/aliexpress.com/get-product
```

## Input

- `product` (string, required): AliExpress product id (the id of Search AliExpress products, e.g. 1005006609803679) or the link of a product page (https://www.aliexpress.com/item/<id>.html, any country site).

## Output

- `url` (string, required)
- `price` (number | null, required): Price of the variant the page selects.
- `title` (string | null, required)
- `currency` (string | null, required)
- `variants` (array, required)
- `available` (boolean, required): True when the product has stock and can be bought.
- `productId` (string, required): The product id AliExpress opened. It can differ from the requested one: the US-site ids (3256...) open the same product under its global id (1005...).
- `images` (array, optional)
- `rating` (number | null, optional)
- `seller` (object, optional)
- `sku_id` (string | null, optional): The variant the page selects; Add AliExpress product to cart adds it when no sku_id is given.
- `sold_text` (string | null, optional)
- `price_text` (string | null, optional)
- `category_id` (string | null, optional)
- `review_count` (integer | null, optional)

## FAQ

### What does "Get AliExpress product" do?

Fetch one AliExpress product from its id or its product page link (as returned by Search AliExpress products). Returns the title, the price and currency of the variant the page selects, availability, rating, review count, sold-count text, images, category, the seller (store name, store id, seller id, positive feedback rate, country) and every variant with its sku id (the id that Add AliExpress product to cart takes), options, price, stock and whether it can be bought. Prices and texts follow the AliExpress site and currency of the browser. An unknown product, or a product AliExpress does not sell in the browser's region, fails with an error that says so; a link that is not a product page fails too.

### How do I automatically get AliExpress product on aliexpress.com?

Ask an AI agent connected to Reduck to run reduck/aliexpress.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/aliexpress.com/get-product

### Is there a aliexpress.com API to get AliExpress product?

You do not need one. "Get AliExpress product" drives the real aliexpress.com pages in a browser, so it works whether or not aliexpress.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns url, price, title, images, rating, seller, sku_id, currency, variants, available, productId, sold_text, price_text, category_id, review_count.

### Do I need to be logged in to aliexpress.com?

No. It only uses pages of aliexpress.com that are reachable without signing in.

### Does it change anything on aliexpress.com, or only read data?

It only reads. It looks things up on aliexpress.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/aliexpress.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/aliexpress.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/aliexpress.com/get-product
