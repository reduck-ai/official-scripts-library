# Get a QVC product

Automatically get a QVC product on qvc.com. Read a QVC product by its item number or page link: price, availability, rating, images, brand and its color and size variants with their ids.

- Site: qvc.com
- Address: `reduck/qvc.com/get-product`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/qvc.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/qvc.com/get-product
```

## Input

- `product` (string, required): QVC item number (e.g. K316571) or a QVC product page link.

## Output

- `id` (string, required)
- `url` (string, required)
- `name` (string | null, required)
- `variants` (array, required)
- `brand` (string | null, optional)
- `price` (number | null, optional): Current lowest selling price.
- `images` (array, optional)
- `rating` (number | null, optional)
- `seller` (string | null, optional)
- `currency` (string | null, optional)
- `max_price` (number | null, optional): Current highest selling price, when variants differ in price.
- `list_price` (number | null, optional): QVC reference price, shown struck through on a sale.
- `description` (string | null, optional)
- `availability` (string, optional)
- `max_quantity` (integer | null, optional): Most units of the product one order can take.
- `review_count` (integer | null, optional)

## FAQ

### What does "Get a QVC product" do?

Read a QVC product by its item number or page link: price, availability, rating, images, brand and its color and size variants with their ids.

### How do I automatically get a QVC product on qvc.com?

Ask an AI agent connected to Reduck to run reduck/qvc.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/qvc.com/get-product

### Is there a qvc.com API to get a QVC product?

You do not need one. "Get a QVC product" drives the real qvc.com pages in a browser, so it works whether or not qvc.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns id, url, name, brand, price, images, rating, seller, currency, variants, max_price, list_price, description, availability, max_quantity, review_count.

### Do I need to be logged in to qvc.com?

No. It only uses pages of qvc.com that are reachable without signing in.

### Does it change anything on qvc.com, or only read data?

It only reads. It looks things up on qvc.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/qvc.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/qvc.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/qvc.com/get-product
