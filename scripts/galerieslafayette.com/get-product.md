# Get Galeries Lafayette product

Automatically get Galeries Lafayette product on galerieslafayette.com. Read one galerieslafayette.com product by its link or code, with its sizes and colours.

- Site: galerieslafayette.com
- Address: `reduck/galerieslafayette.com/get-product`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/galerieslafayette.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/galerieslafayette.com/get-product
```

## Input

- `product` (string, required): A galerieslafayette.com product link (https://www.galerieslafayette.com/p/...) or a product code from search-products.

## Output

- `id` (string, required): Code of this colour
- `url` (string, required)
- `name` (string | null, required)
- `price` (number | null, required)
- `currency` (string, required)
- `variants` (array, required): Buyable sizes of this colour (or the colour itself when it has no sizes)
- `brand` (string | null, optional)
- `color` (string | null, optional)
- `seller` (string | null, optional)
- `categories` (array, optional)
- `image_urls` (array, optional)
- `list_price` (number | null, optional)
- `description` (string | null, optional)
- `marketplace` (boolean, optional)
- `offers_count` (integer, optional)
- `discount_percent` (number | null, optional)

## FAQ

### What does "Get Galeries Lafayette product" do?

Read one galerieslafayette.com product by its link or code, with its sizes and colours.

### How do I automatically get Galeries Lafayette product on galerieslafayette.com?

Ask an AI agent connected to Reduck to run reduck/galerieslafayette.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/galerieslafayette.com/get-product

### Is there a galerieslafayette.com API to get Galeries Lafayette product?

You do not need one. "Get Galeries Lafayette product" drives the real galerieslafayette.com pages in a browser, so it works whether or not galerieslafayette.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns id, url, name, brand, color, price, seller, currency, variants, categories, image_urls, list_price, description, marketplace, offers_count, discount_percent.

### Do I need to be logged in to galerieslafayette.com?

No. It only uses pages of galerieslafayette.com that are reachable without signing in.

### Does it change anything on galerieslafayette.com, or only read data?

It only reads. It looks things up on galerieslafayette.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/galerieslafayette.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/galerieslafayette.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/galerieslafayette.com/get-product
