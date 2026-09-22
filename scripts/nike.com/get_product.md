# Get Nike product

Automatically get Nike product on nike.com. Fetch a Nike product page by URL. Returns name, brand, styleColor, description, colors, selectedColor, sizes (with size, mpn, price, currency, availability), and productGroupId. The URL must be a Nike product page (a /t/ path), not a search or category page.

- Site: nike.com
- Address: `reduck/nike.com/get_product`
- Updated: 2026-08-26 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/nike.com/get_product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/nike.com/get_product
```

## Input

- `url` (string, required)

## Output

- `url` (string, required)
- `name` (string, required)
- `styleColor` (string, required)
- `brand` (string | null, optional)
- `sizes` (array, optional)
- `colors` (array, optional)
- `description` (string | null, optional)
- `selectedColor` (object | null, optional)
- `productGroupId` (string | null, optional)

## FAQ

### What does "Get Nike product" do?

Fetch a Nike product page by URL. Returns name, brand, styleColor, description, colors, selectedColor, sizes (with size, mpn, price, currency, availability), and productGroupId. The URL must be a Nike product page (a /t/ path), not a search or category page.

### How do I automatically get Nike product on nike.com?

Ask an AI agent connected to Reduck to run reduck/nike.com/get_product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/nike.com/get_product

### Is there a nike.com API to get Nike product?

You do not need one. "Get Nike product" drives the real nike.com pages in a browser, so it works whether or not nike.com offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns url, name, brand, sizes, colors, styleColor, description, selectedColor, productGroupId.

### Do I need to be logged in to nike.com?

No. It only uses pages of nike.com that are reachable without signing in.

### Does it change anything on nike.com, or only read data?

It only reads. It looks things up on nike.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/nike.com/get_product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/nike.com/get_product

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/nike.com/get_product
