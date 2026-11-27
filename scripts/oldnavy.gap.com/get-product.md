# Get Old Navy product

Automatically get Old Navy product on oldnavy.gap.com. Get one product of the Old Navy US store (oldnavy.gap.com) from its id or its product page link: the product id, name, brand, description and detail lines, rating and rating count, the fits (for example Regular, Tall, Petite) and size labels, every color with its id, name, price, regular price, stock status and image, and every size variant with its offerId (the sku), color, fit, size, price, regular price in US dollars and stock. Pass offerId and productId to Add a product to the Old Navy cart. A product page can hold several colors that Old Navy names differently: name is the name of the color the page shows (selectedColorId), and each color has its own title. An id or link that Old Navy does not know fails with a message that says so.

- Site: oldnavy.gap.com
- Address: `reduck/oldnavy.gap.com/get-product`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/oldnavy.gap.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/oldnavy.gap.com/get-product
```

## Input

- `url` (string, optional): Link of an Old Navy product page, for example https://oldnavy.gap.com/browse/product.do?pid=788099002. Give productId or url.
- `productId` (string, optional): Old Navy product id (for example "788099"), color id (for example "788099002") or sku (offerId), as returned by Search Old Navy products or Get Old Navy product. Give productId or url.

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

### What does "Get Old Navy product" do?

Get one product of the Old Navy US store (oldnavy.gap.com) from its id or its product page link: the product id, name, brand, description and detail lines, rating and rating count, the fits (for example Regular, Tall, Petite) and size labels, every color with its id, name, price, regular price, stock status and image, and every size variant with its offerId (the sku), color, fit, size, price, regular price in US dollars and stock. Pass offerId and productId to Add a product to the Old Navy cart. A product page can hold several colors that Old Navy names differently: name is the name of the color the page shows (selectedColorId), and each color has its own title. An id or link that Old Navy does not know fails with a message that says so.

### How do I automatically get Old Navy product on oldnavy.gap.com?

Ask an AI agent connected to Reduck to run reduck/oldnavy.gap.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/oldnavy.gap.com/get-product

### Is there a oldnavy.gap.com API to get Old Navy product?

You do not need one. "Get Old Navy product" drives the real oldnavy.gap.com pages in a browser, so it works whether or not oldnavy.gap.com offers an API for this.

### What information do I need to provide?

Optional: url, productId.

### What does it return?

It returns url, fits, name, brand, colors, rating, details, variants, productId, sizeLabels, description, reviewCount, selectedColorId.

### Do I need to be logged in to oldnavy.gap.com?

No. It only uses pages of oldnavy.gap.com that are reachable without signing in.

### Does it change anything on oldnavy.gap.com, or only read data?

It only reads. It looks things up on oldnavy.gap.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/oldnavy.gap.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/oldnavy.gap.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/oldnavy.gap.com/get-product
