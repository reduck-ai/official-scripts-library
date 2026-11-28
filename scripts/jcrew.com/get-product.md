# Get J.Crew product

Automatically get J.Crew product on jcrew.com. Get one J.Crew (jcrew.com, US) product from its code or its product page link: code, link, name, brand, gender, description and detail lines, list price in US dollars, rating out of 5 and review count, whether it is a preorder or sold out, the most units one order can hold, category path, every color with its code, name and price, the sizes, and every offer (one color in one size) with its offerId (the sku), color code, color, size, list price, price and stock. Sold-out offers are listed with in_stock false. An unknown code or a link that is not a J.Crew product page fails with a message that says so.

- Site: jcrew.com
- Address: `reduck/jcrew.com/get-product`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/jcrew.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/jcrew.com/get-product
```

## Input

- `product` (string, required): Product code (the last part of a product link, for example CX405) or the product link.

## Output

- `id` (string, required): Product code.
- `url` (string, required)
- `name` (string, required)
- `brand` (string | null, required)
- `sizes` (array, required)
- `colors` (array, required)
- `gender` (string | null, required)
- `rating` (number | null, required): Average customer rating out of 5.
- `details` (array, required)
- `preorder` (boolean | null, required)
- `variants` (array, required)
- `list_price` (number | null, required): Full price in US dollars.
- `breadcrumbs` (array, required)
- `description` (string | null, required)
- `max_quantity` (integer | null, required): Most units of the product one order can hold.
- `out_of_stock` (boolean | null, required)
- `review_count` (integer | null, required)

## FAQ

### What does "Get J.Crew product" do?

Get one J.Crew (jcrew.com, US) product from its code or its product page link: code, link, name, brand, gender, description and detail lines, list price in US dollars, rating out of 5 and review count, whether it is a preorder or sold out, the most units one order can hold, category path, every color with its code, name and price, the sizes, and every offer (one color in one size) with its offerId (the sku), color code, color, size, list price, price and stock. Sold-out offers are listed with in_stock false. An unknown code or a link that is not a J.Crew product page fails with a message that says so.

### How do I automatically get J.Crew product on jcrew.com?

Ask an AI agent connected to Reduck to run reduck/jcrew.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/jcrew.com/get-product

### Is there a jcrew.com API to get J.Crew product?

You do not need one. "Get J.Crew product" drives the real jcrew.com pages in a browser, so it works whether or not jcrew.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns id, url, name, brand, sizes, colors, gender, rating, details, preorder, variants, list_price, breadcrumbs, description, max_quantity, out_of_stock, review_count.

### Do I need to be logged in to jcrew.com?

No. It only uses pages of jcrew.com that are reachable without signing in.

### Does it change anything on jcrew.com, or only read data?

It only reads. It looks things up on jcrew.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/jcrew.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/jcrew.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/jcrew.com/get-product
