# Get Gap product

Automatically get Gap product on gap.com. Get one product of the Gap US store (gap.com) from its id or its product page link: the product id, name, brand, description and detail lines, rating and rating count, the fits (for example Regular, Tall, Petite) and size labels, every color with its id, name, price, regular price, stock status and image, and every size variant with its offerId (the sku), color, fit, size, price, regular price in US dollars and stock. Pass offerId and productId to Add a product to the Gap cart. A product page can hold several colors that Gap names differently: name is the name of the color the page shows (selectedColorId), and each color has its own title. An id or link that Gap does not know fails with a message that says so.

- Site: gap.com
- Address: `reduck/gap.com/get-product`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/gap.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/gap.com/get-product
```

## Input

- `url` (string, optional): Link of a Gap product page, for example https://www.gap.com/browse/product.do?pid=403540002. Give productId or url.
- `productId` (string, optional): Gap product id (for example "403540"), color id (for example "403540002") or sku (offerId), as returned by Search Gap products or Get Gap product. Give productId or url.

## Output

- `url` (string, required)
- `name` (string | null, required)
- `colors` (array, required)
- `variants` (array, required)
- `productId` (string, required)
- `selectedColorId` (string | null, required)
- `fits` (array, optional)
- `brand` (string | null, optional)
- `rating` (number | null, optional)
- `details` (array, optional)
- `sizeLabels` (array, optional)
- `description` (string | null, optional)
- `reviewCount` (integer | null, optional)

## FAQ

### What does "Get Gap product" do?

Get one product of the Gap US store (gap.com) from its id or its product page link: the product id, name, brand, description and detail lines, rating and rating count, the fits (for example Regular, Tall, Petite) and size labels, every color with its id, name, price, regular price, stock status and image, and every size variant with its offerId (the sku), color, fit, size, price, regular price in US dollars and stock. Pass offerId and productId to Add a product to the Gap cart. A product page can hold several colors that Gap names differently: name is the name of the color the page shows (selectedColorId), and each color has its own title. An id or link that Gap does not know fails with a message that says so.

### How do I automatically get Gap product on gap.com?

Ask an AI agent connected to Reduck to run reduck/gap.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gap.com/get-product

### Is there a gap.com API to get Gap product?

You do not need one. "Get Gap product" drives the real gap.com pages in a browser, so it works whether or not gap.com offers an API for this.

### What information do I need to provide?

Optional: url, productId.

### What does it return?

It returns url, fits, name, brand, colors, rating, details, variants, productId, sizeLabels, description, reviewCount, selectedColorId.

### Do I need to be logged in to gap.com?

No. It only uses pages of gap.com that are reachable without signing in.

### Does it change anything on gap.com, or only read data?

It only reads. It looks things up on gap.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/gap.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gap.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/gap.com/get-product
