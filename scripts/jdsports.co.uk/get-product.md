# Get JD Sports product

Automatically get JD Sports product on jdsports.co.uk. Get one product of JD Sports UK (jdsports.co.uk, the United Kingdom store) from its JD Sports product id or product page link: name, brand, colour, description, link, category, images, price and earlier price in pounds (GBP), whether it is on sale or out of stock, and every size with its sku (the offer id the cart uses), barcode number, price, earlier price and whether it is available. An id that is not a JD Sports product fails with an error that says so.

- Site: jdsports.co.uk
- Address: `reduck/jdsports.co.uk/get-product`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/jdsports.co.uk/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/jdsports.co.uk/get-product
```

## Input

- `product` (string, required): A JD Sports product id as Search JD Sports products returns it, for example 19760893, or a jdsports.co.uk product page link.

## Output

- `url` (string | null, required)
- `name` (string | null, required)
- `brand` (string | null, required)
- `price` (number | null, required): The lowest price of the sizes, in the currency given.
- `colour` (string | null, required)
- `onSale` (boolean | null, required)
- `category` (string | null, required)
- `currency` (string | null, required)
- `variants` (array, required): The sizes of the product.
- `wasPrice` (number | null, required): The lowest earlier price of the sizes.
- `imageUrls` (array, required)
- `productId` (string, required)
- `outOfStock` (boolean | null, required)
- `description` (string | null, required)

## FAQ

### What does "Get JD Sports product" do?

Get one product of JD Sports UK (jdsports.co.uk, the United Kingdom store) from its JD Sports product id or product page link: name, brand, colour, description, link, category, images, price and earlier price in pounds (GBP), whether it is on sale or out of stock, and every size with its sku (the offer id the cart uses), barcode number, price, earlier price and whether it is available. An id that is not a JD Sports product fails with an error that says so.

### How do I automatically get JD Sports product on jdsports.co.uk?

Ask an AI agent connected to Reduck to run reduck/jdsports.co.uk/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/jdsports.co.uk/get-product

### Is there a jdsports.co.uk API to get JD Sports product?

You do not need one. "Get JD Sports product" drives the real jdsports.co.uk pages in a browser, so it works whether or not jdsports.co.uk offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns url, name, brand, price, colour, onSale, category, currency, variants, wasPrice, imageUrls, productId, outOfStock, description.

### Do I need to be logged in to jdsports.co.uk?

No. It only uses pages of jdsports.co.uk that are reachable without signing in.

### Does it change anything on jdsports.co.uk, or only read data?

It only reads. It looks things up on jdsports.co.uk and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/jdsports.co.uk/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/jdsports.co.uk/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/jdsports.co.uk/get-product
