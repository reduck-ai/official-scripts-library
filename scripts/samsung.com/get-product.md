# Get Samsung product

Automatically get Samsung product on samsung.com. Get a product of the Samsung US store (samsung.com/us) by its model code (SKU) or its product link. Returns the model asked for (name, family, category, link, sale and regular price in US dollars, stock status, rating, review count, images) and every configuration of its product family (color, storage, size, carrier...), each with its own model code to pass to Add a product to the Samsung cart, its options, price, stock status and link. A link to a product family page with no model code in it, a link that is not a Samsung US product link, and a model code Samsung US does not sell fail with an error that says so.

- Site: samsung.com
- Address: `reduck/samsung.com/get-product`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/samsung.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/samsung.com/get-product
```

## Input

- `url` (string, optional): Samsung US product link that ends with the model code, for example https://www.samsung.com/us/smartphones/galaxy-s26-ultra/buy/galaxy-s26-ultra-256gb-unlocked-sku-sm-s948uzvaxaa. Used when no product_id is given.
- `product_id` (string, optional): Samsung model code (SKU), for example SM-S948UZVAXAA, as productId of Search Samsung products.

## Output

- `url` (string | null, required)
- `name` (string, required)
- `variants` (array, required)
- `productId` (string, required): Model code (SKU) of the product.
- `badge` (string | null, optional)
- `price` (number | null, optional): Sale price in US dollars.
- `images` (array, optional)
- `rating` (number | null, optional)
- `offerId` (string | null, optional): Shop SKU that the cart takes for this model.
- `options` (array, optional): Option types of the family and their values.
- `category` (string | null, optional)
- `currency` (string | null, optional)
- `familyId` (string | null, optional)
- `selected` (array, optional)
- `buyButton` (string | null, optional): The action the product page offers, as the site names it (for example inStock or learnMore).
- `modelName` (string | null, optional)
- `familyName` (string | null, optional)
- `reviewCount` (integer | null, optional)
- `stockStatus` (string | null, optional)
- `regularPrice` (number | null, optional): Price before discount in US dollars.

## FAQ

### What does "Get Samsung product" do?

Get a product of the Samsung US store (samsung.com/us) by its model code (SKU) or its product link. Returns the model asked for (name, family, category, link, sale and regular price in US dollars, stock status, rating, review count, images) and every configuration of its product family (color, storage, size, carrier...), each with its own model code to pass to Add a product to the Samsung cart, its options, price, stock status and link. A link to a product family page with no model code in it, a link that is not a Samsung US product link, and a model code Samsung US does not sell fail with an error that says so.

### How do I automatically get Samsung product on samsung.com?

Ask an AI agent connected to Reduck to run reduck/samsung.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/samsung.com/get-product

### Is there a samsung.com API to get Samsung product?

You do not need one. "Get Samsung product" drives the real samsung.com pages in a browser, so it works whether or not samsung.com offers an API for this.

### What information do I need to provide?

Optional: url, product_id.

### What does it return?

It returns url, name, badge, price, images, rating, offerId, options, category, currency, familyId, selected, variants, buyButton, modelName, productId, familyName, reviewCount, stockStatus, regularPrice.

### Do I need to be logged in to samsung.com?

No. It only uses pages of samsung.com that are reachable without signing in.

### Does it change anything on samsung.com, or only read data?

It only reads. It looks things up on samsung.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/samsung.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/samsung.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/samsung.com/get-product
