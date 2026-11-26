# Get Apple Store product

Automatically get Apple Store product on apple.com. Read one Apple Store (US) product page from its part number or link: name, price, availability, brand, images, rating and the color or size options with their part numbers.

- Site: apple.com
- Address: `reduck/apple.com/get-product`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/apple.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/apple.com/get-product
```

## Input

- `product` (string, required): Apple part number (for example MEQL4LL/A) or a product page link such as https://www.apple.com/shop/product/MEQL4LL/A.

## Output

- `id` (string, required): Apple part number.
- `url` (string, required)
- `images` (array, required)
- `variants` (array, required)
- `name` (string | null, optional)
- `brand` (string | null, optional)
- `color` (string | null, optional)
- `price` (number | null, optional)
- `rating` (number | null, optional)
- `seller` (string | null, optional)
- `currency` (string | null, optional)
- `available` (boolean | null, optional): True when the page lets you add the product to the bag.
- `list_price` (number | null, optional): Price before a discount, when the page shows one.
- `description` (string | null, optional)
- `availability` (string | null, optional): schema.org availability, for example InStock.
- `review_count` (integer | null, optional)

## FAQ

### What does "Get Apple Store product" do?

Read one Apple Store (US) product page from its part number or link: name, price, availability, brand, images, rating and the color or size options with their part numbers.

### How do I automatically get Apple Store product on apple.com?

Ask an AI agent connected to Reduck to run reduck/apple.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/apple.com/get-product

### Is there a apple.com API to get Apple Store product?

You do not need one. "Get Apple Store product" drives the real apple.com pages in a browser, so it works whether or not apple.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns id, url, name, brand, color, price, images, rating, seller, currency, variants, available, list_price, description, availability, review_count.

### Do I need to be logged in to apple.com?

No. It only uses pages of apple.com that are reachable without signing in.

### Does it change anything on apple.com, or only read data?

It only reads. It looks things up on apple.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/apple.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/apple.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/apple.com/get-product
