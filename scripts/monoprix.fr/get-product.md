# Get Monoprix product

Automatically get Monoprix product on monoprix.fr. Read one monoprix.fr product by its link.

- Site: monoprix.fr
- Address: `reduck/monoprix.fr/get-product`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/monoprix.fr/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/monoprix.fr/get-product
```

## Input

- `product` (string, required): A courses.monoprix.fr product link, or its id like MPX_875909 (from search-products).

## Output

- `id` (string, required)
- `url` (string, required)
- `name` (string, required)
- `price` (number | null, required)
- `currency` (string | null, required)
- `available` (boolean, required)
- `unit` (string | null, optional)
- `brand` (string | null, optional)
- `details` (object, optional): Labelled facts from the product sheet, e.g. ingredients, allergens, manufacturer
- `pack_size` (string | null, optional)
- `image_urls` (array, optional)
- `unit_price` (number | null, optional)
- `description` (string | null, optional): Product description as plain text
- `product_uuid` (string, optional)

## FAQ

### What does "Get Monoprix product" do?

Read one monoprix.fr product by its link.

### How do I automatically get Monoprix product on monoprix.fr?

Ask an AI agent connected to Reduck to run reduck/monoprix.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/monoprix.fr/get-product

### Is there a monoprix.fr API to get Monoprix product?

You do not need one. "Get Monoprix product" drives the real monoprix.fr pages in a browser, so it works whether or not monoprix.fr offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns id, url, name, unit, brand, price, details, currency, available, pack_size, image_urls, unit_price, description, product_uuid.

### Do I need to be logged in to monoprix.fr?

No. It only uses pages of monoprix.fr that are reachable without signing in.

### Does it change anything on monoprix.fr, or only read data?

It only reads. It looks things up on monoprix.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/monoprix.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/monoprix.fr/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/monoprix.fr/get-product
