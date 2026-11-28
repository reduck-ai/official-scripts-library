# Get a Nykaa product

Automatically get a Nykaa product on nykaa.com. Get one product of the Nykaa India store (nykaa.com) by its product id or its link: name, brand, price and maximum retail price in Indian rupees, discount, stock, rating, seller, pack size, expiry date, country of origin, categories, pictures, description, how to use, ingredients, offers, and each shade or size with its own id, price and stock. Give variantId to read one shade or size. An unknown id gives an error that says Nykaa has no such product.

- Site: nykaa.com
- Address: `reduck/nykaa.com/get-product`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/nykaa.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/nykaa.com/get-product
```

## Input

- `url` (string, optional): Product page link on nykaa.com. Give productId or url.
- `productId` (string, optional): Nykaa product id: the number after /p/ in the product link, as search-products returns it.
- `variantId` (string, optional): Id of a shade or size of the product. Its price and stock fill the top fields.

## Output

- `url` (string, required)
- `name` (string, required)
- `variants` (array, required)
- `productId` (string, required)
- `mrp` (number | null, optional): Maximum retail price in Indian rupees.
- `brand` (string | null, optional)
- `price` (number | null, optional): Selling price in Indian rupees.
- `expiry` (string | null, optional): Expiry date as the page shows it.
- `offers` (array, optional)
- `rating` (number | null, optional)
- `seller` (string | null, optional): Seller that the product page names.
- `inStock` (boolean | null, optional)
- `currency` (string, optional): INR
- `howToUse` (string | null, optional)
- `packSize` (string | null, optional)
- `imageUrls` (array, optional)
- `categories` (array, optional)
- `description` (string | null, optional)
- `ingredients` (string | null, optional)
- `productType` (string | null, optional)
- `ratingCount` (integer | null, optional)
- `reviewCount` (integer | null, optional)
- `variantType` (string | null, optional)
- `countryOfOrigin` (string | null, optional)
- `discountPercent` (number | null, optional)
- `selectedVariantId` (string | null, optional): Shade or size that the price, stock and pack size fields describe.
- `selectedVariantName` (string | null, optional)

## FAQ

### What does "Get a Nykaa product" do?

Get one product of the Nykaa India store (nykaa.com) by its product id or its link: name, brand, price and maximum retail price in Indian rupees, discount, stock, rating, seller, pack size, expiry date, country of origin, categories, pictures, description, how to use, ingredients, offers, and each shade or size with its own id, price and stock. Give variantId to read one shade or size. An unknown id gives an error that says Nykaa has no such product.

### How do I automatically get a Nykaa product on nykaa.com?

Ask an AI agent connected to Reduck to run reduck/nykaa.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/nykaa.com/get-product

### Is there a nykaa.com API to get a Nykaa product?

You do not need one. "Get a Nykaa product" drives the real nykaa.com pages in a browser, so it works whether or not nykaa.com offers an API for this.

### What information do I need to provide?

Optional: url, productId, variantId.

### What does it return?

It returns mrp, url, name, brand, price, expiry, offers, rating, seller, inStock, currency, howToUse, packSize, variants, imageUrls, productId, categories, description, ingredients, productType, ratingCount, reviewCount, variantType, countryOfOrigin, discountPercent, selectedVariantId, selectedVariantName.

### Do I need to be logged in to nykaa.com?

No. It only uses pages of nykaa.com that are reachable without signing in.

### Does it change anything on nykaa.com, or only read data?

It only reads. It looks things up on nykaa.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/nykaa.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/nykaa.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/nykaa.com/get-product
