# Get ASOS product

Automatically get ASOS product on asos.com. Read one product of the ASOS UK store (asos.com) from its product id or product page link: name, brand, product type, fit, colour, price, price before a reduction, recommended retail price, lowest price in the last 30 days and discount in pounds, stock, rating and review count, description, size and fit, care and material text, category path, images, every size with its variant id, SKU, barcode number, stock, seller and price, and the other colours of the product with their product ids. An id or link that ASOS does not know fails with a message that says so.

- Site: asos.com
- Address: `reduck/asos.com/get-product`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/asos.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/asos.com/get-product
```

## Input

- `product` (string, required): ASOS product id (for example 210529423, the productId of Search ASOS products) or an asos.com product page link.

## Output

- `fit` (string | null, required)
- `link` (string, required)
- `name` (string | null, required)
- `brand` (string | null, required)
- `price` (number | null, required): Price now, in the currency of the store (GBP on the UK store).
- `colour` (string | null, required)
- `gender` (string | null, required)
- `images` (array, required)
- `rating` (number | null, required): Average rating out of 5.
- `aboutMe` (string | null, required): Material text of the page.
- `inStock` (boolean, required): True when at least one size is in stock.
- `oneSize` (boolean, required)
- `careInfo` (string | null, required)
- `currency` (string, required)
- `variants` (array, required): Every size of the product.
- `productId` (string, required)
- `categories` (array, required): Category path of the page, from the top.
- `sizeAndFit` (string | null, required)
- `description` (string | null, required)
- `productCode` (string | null, required): ASOS product code, as shown on the page.
- `productType` (string | null, required)
- `reviewCount` (integer | null, required)
- `sellingFast` (boolean, required)
- `discontinued` (boolean, required)
- `otherColours` (array, required): The same product in other colours.
- `previousPrice` (number | null, required): Price before the reduction, when the product is reduced.
- `brandDescription` (string | null, required)
- `discountPercentage` (number | null, required)
- `countryOfManufacture` (string | null, required): Country code.
- `percentageRecommended` (number | null, required)
- `recommendedRetailPrice` (number | null, required)
- `lowestPriceInLast30Days` (number | null, required)

## FAQ

### What does "Get ASOS product" do?

Read one product of the ASOS UK store (asos.com) from its product id or product page link: name, brand, product type, fit, colour, price, price before a reduction, recommended retail price, lowest price in the last 30 days and discount in pounds, stock, rating and review count, description, size and fit, care and material text, category path, images, every size with its variant id, SKU, barcode number, stock, seller and price, and the other colours of the product with their product ids. An id or link that ASOS does not know fails with a message that says so.

### How do I automatically get ASOS product on asos.com?

Ask an AI agent connected to Reduck to run reduck/asos.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/asos.com/get-product

### Is there a asos.com API to get ASOS product?

You do not need one. "Get ASOS product" drives the real asos.com pages in a browser, so it works whether or not asos.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns fit, link, name, brand, price, colour, gender, images, rating, aboutMe, inStock, oneSize, careInfo, currency, variants, productId, categories, sizeAndFit, description, productCode, productType, reviewCount, sellingFast, discontinued, otherColours, previousPrice, brandDescription, discountPercentage, countryOfManufacture, percentageRecommended, recommendedRetailPrice, lowestPriceInLast30Days.

### Do I need to be logged in to asos.com?

No. It only uses pages of asos.com that are reachable without signing in.

### Does it change anything on asos.com, or only read data?

It only reads. It looks things up on asos.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/asos.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/asos.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/asos.com/get-product
