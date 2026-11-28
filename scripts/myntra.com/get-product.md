# Get Myntra product

Automatically get Myntra product on myntra.com. Read one myntra.com product by its link: name, brand, price and MRP in rupees, colour, category, gender, country of origin, rating, rating count, details, images, sellers, and every size with its sku, price and availability. Takes the link Search Myntra products returns.

- Site: myntra.com
- Address: `reduck/myntra.com/get-product`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/myntra.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/myntra.com/get-product
```

## Input

- `url` (string, required): The product's link as Search Myntra products returns it (https://www.myntra.com/.../<id>/buy).

## Output

- `id` (string, required)
- `url` (string, required)
- `name` (string, required)
- `sizes` (array, required)
- `mrp` (number | null, optional)
- `brand` (string | null, optional)
- `price` (number | null, optional)
- `colour` (string | null, optional)
- `gender` (string | null, optional)
- `images` (array, optional)
- `rating` (number | null, optional)
- `details` (array, optional)
- `sellers` (array, optional)
- `category` (string | null, optional)
- `currency` (string, optional)
- `rating_count` (integer | null, optional)
- `country_of_origin` (string | null, optional)

## FAQ

### What does "Get Myntra product" do?

Read one myntra.com product by its link: name, brand, price and MRP in rupees, colour, category, gender, country of origin, rating, rating count, details, images, sellers, and every size with its sku, price and availability. Takes the link Search Myntra products returns.

### How do I automatically get Myntra product on myntra.com?

Ask an AI agent connected to Reduck to run reduck/myntra.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/myntra.com/get-product

### Is there a myntra.com API to get Myntra product?

You do not need one. "Get Myntra product" drives the real myntra.com pages in a browser, so it works whether or not myntra.com offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns id, mrp, url, name, brand, price, sizes, colour, gender, images, rating, details, sellers, category, currency, rating_count, country_of_origin.

### Do I need to be logged in to myntra.com?

No. It only uses pages of myntra.com that are reachable without signing in.

### Does it change anything on myntra.com, or only read data?

It only reads. It looks things up on myntra.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/myntra.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/myntra.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/myntra.com/get-product
