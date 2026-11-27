# Get Athleta product

Automatically get Athleta product on athleta.gap.com. Get one product of the Athleta US store (athleta.gap.com) from its id or its product page link: the product id, name, brand, description and detail lines, rating and rating count, the fits (for example Regular, Tall, Petite) and size labels, every color with its id, name, price, regular price, stock status and image, and every size variant with its offerId (the sku), color, fit, size, price, regular price in US dollars and stock. Pass offerId and productId to Add a product to the Athleta cart. A product page can hold several colors that Athleta names differently: name is the name of the color the page shows (selectedColorId), and each color has its own title. An id or link that Athleta does not know fails with a message that says so.

- Site: athleta.gap.com
- Address: `reduck/athleta.gap.com/get-product`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/athleta.gap.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/athleta.gap.com/get-product
```

## Input

- `url` (string, optional): Link of an Athleta product page, for example https://athleta.gap.com/browse/product.do?pid=1190608032. Give productId or url.
- `productId` (string, optional): Athleta product id (for example "1190608"), color id (for example "1190608032") or sku (offerId), as returned by Search Athleta products or Get Athleta product. Give productId or url.

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

### What does "Get Athleta product" do?

Get one product of the Athleta US store (athleta.gap.com) from its id or its product page link: the product id, name, brand, description and detail lines, rating and rating count, the fits (for example Regular, Tall, Petite) and size labels, every color with its id, name, price, regular price, stock status and image, and every size variant with its offerId (the sku), color, fit, size, price, regular price in US dollars and stock. Pass offerId and productId to Add a product to the Athleta cart. A product page can hold several colors that Athleta names differently: name is the name of the color the page shows (selectedColorId), and each color has its own title. An id or link that Athleta does not know fails with a message that says so.

### How do I automatically get Athleta product on athleta.gap.com?

Ask an AI agent connected to Reduck to run reduck/athleta.gap.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/athleta.gap.com/get-product

### Is there a athleta.gap.com API to get Athleta product?

You do not need one. "Get Athleta product" drives the real athleta.gap.com pages in a browser, so it works whether or not athleta.gap.com offers an API for this.

### What information do I need to provide?

Optional: url, productId.

### What does it return?

It returns url, fits, name, brand, colors, rating, details, variants, productId, sizeLabels, description, reviewCount, selectedColorId.

### Do I need to be logged in to athleta.gap.com?

No. It only uses pages of athleta.gap.com that are reachable without signing in.

### Does it change anything on athleta.gap.com, or only read data?

It only reads. It looks things up on athleta.gap.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/athleta.gap.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/athleta.gap.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/athleta.gap.com/get-product
