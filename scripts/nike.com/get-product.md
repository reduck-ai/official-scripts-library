# Get Nike product

Automatically get Nike product on nike.com. Read one Nike.com (US) product from its style-color id (e.g. CN8490-100, as Search Nike products returns) or its /t/ product link: title, subtitle, description, price and list price in USD, color, buy status, every size with its availability and sku id, the other colorways and the images. An unknown id fails with an error that says so.

- Site: nike.com
- Address: `reduck/nike.com/get-product`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/nike.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/nike.com/get-product
```

## Input

- `product` (string, required): A style-color id such as CN8490-100, or a nike.com/t/ product link.

## Output

- `id` (string, required)
- `url` (string, required)
- `price` (number | null, required)
- `sizes` (array, required)
- `title` (string, required)
- `currency` (string, required)
- `color` (string | null, optional)
- `images` (array, optional)
- `status` (string | null, optional)
- `subtitle` (string | null, optional)
- `colorways` (array, optional)
- `group_key` (string | null, optional)
- `list_price` (number | null, optional)
- `description` (string | null, optional)

## FAQ

### What does "Get Nike product" do?

Read one Nike.com (US) product from its style-color id (e.g. CN8490-100, as Search Nike products returns) or its /t/ product link: title, subtitle, description, price and list price in USD, color, buy status, every size with its availability and sku id, the other colorways and the images. An unknown id fails with an error that says so.

### How do I automatically get Nike product on nike.com?

Ask an AI agent connected to Reduck to run reduck/nike.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/nike.com/get-product

### Is there a nike.com API to get Nike product?

You do not need one. "Get Nike product" drives the real nike.com pages in a browser, so it works whether or not nike.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns id, url, color, price, sizes, title, images, status, currency, subtitle, colorways, group_key, list_price, description.

### Do I need to be logged in to nike.com?

No. It only uses pages of nike.com that are reachable without signing in.

### Does it change anything on nike.com, or only read data?

It only reads. It looks things up on nike.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/nike.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/nike.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/nike.com/get-product
