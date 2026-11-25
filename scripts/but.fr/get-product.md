# Get BUT.fr product

Automatically get BUT.fr product on but.fr. Fetch one BUT.fr product page by its product id or link (the id that Search BUT products returns, for example 4894223246194). Returns title, brand, EAN, price and struck-through list price in euros with the discount, rating and review count, the seller, a short description, the images, the breadcrumb, and the availability (whether it can be bought online, the stock and the fastest home delivery with its cost). An unknown product fails with an error that says so.

- Site: but.fr
- Address: `reduck/but.fr/get-product`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/but.fr/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/but.fr/get-product
```

## Input

- `product` (string, required): Link of a BUT.fr product page or its product id (4894223246194), as Search BUT products gives it.

## Output

- `id` (string, required)
- `ean` (string | null, required)
- `url` (string, required)
- `name` (string | null, required)
- `brand` (string | null, required)
- `price` (number | null, required): Price in euros, taxes included.
- `images` (array, required)
- `rating` (number | null, required)
- `seller` (string | null, required)
- `currency` (string | null, required)
- `breadcrumb` (array, required)
- `list_price` (number | null, required): Struck-through price in euros.
- `description` (string | null, required)
- `availability` (object, required)
- `review_count` (integer | null, required)
- `discount_percent` (number | null, required)

## FAQ

### What does "Get BUT.fr product" do?

Fetch one BUT.fr product page by its product id or link (the id that Search BUT products returns, for example 4894223246194). Returns title, brand, EAN, price and struck-through list price in euros with the discount, rating and review count, the seller, a short description, the images, the breadcrumb, and the availability (whether it can be bought online, the stock and the fastest home delivery with its cost). An unknown product fails with an error that says so.

### How do I automatically get BUT.fr product on but.fr?

Ask an AI agent connected to Reduck to run reduck/but.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/but.fr/get-product

### Is there a but.fr API to get BUT.fr product?

You do not need one. "Get BUT.fr product" drives the real but.fr pages in a browser, so it works whether or not but.fr offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns id, ean, url, name, brand, price, images, rating, seller, currency, breadcrumb, list_price, description, availability, review_count, discount_percent.

### Do I need to be logged in to but.fr?

No. It only uses pages of but.fr that are reachable without signing in.

### Does it change anything on but.fr, or only read data?

It only reads. It looks things up on but.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/but.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/but.fr/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/but.fr/get-product
