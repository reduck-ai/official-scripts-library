# Get La Redoute product

Automatically get La Redoute product on laredoute.fr. Read one La Redoute product by its link: name, brand, prices in euros, discount, rating, review count, stock, delivery fee, return days, description, images, and every variant (colour and size) with its id, reference, barcode, price, stock, delivery delay and seller. Takes the link Search La Redoute products returns.

- Site: laredoute.fr
- Address: `reduck/laredoute.fr/get-product`
- Updated: 2026-11-27 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/laredoute.fr/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/laredoute.fr/get-product
```

## Input

- `url` (string, required): The product's link as Search La Redoute products returns it (https://www.laredoute.fr/ppdp/prod-<id>.aspx).

## Output

- `id` (string, required)
- `url` (string, required)
- `name` (string, required)
- `variants` (array, required)
- `brand` (string | null, optional)
- `price` (number | null, optional)
- `images` (array, optional)
- `rating` (number | null, optional)
- `currency` (string, optional)
- `old_price` (number | null, optional)
- `description` (string | null, optional)
- `return_days` (integer | null, optional)
- `availability` (string | null, optional)
- `review_count` (integer | null, optional)
- `shipping_fee` (number | null, optional)
- `discount_percent` (number | null, optional)

## FAQ

### What does "Get La Redoute product" do?

Read one La Redoute product by its link: name, brand, prices in euros, discount, rating, review count, stock, delivery fee, return days, description, images, and every variant (colour and size) with its id, reference, barcode, price, stock, delivery delay and seller. Takes the link Search La Redoute products returns.

### How do I automatically get La Redoute product on laredoute.fr?

Ask an AI agent connected to Reduck to run reduck/laredoute.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/laredoute.fr/get-product

### Is there a laredoute.fr API to get La Redoute product?

You do not need one. "Get La Redoute product" drives the real laredoute.fr pages in a browser, so it works whether or not laredoute.fr offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns id, url, name, brand, price, images, rating, currency, variants, old_price, description, return_days, availability, review_count, shipping_fee, discount_percent.

### Do I need to be logged in to laredoute.fr?

No. It only uses pages of laredoute.fr that are reachable without signing in.

### Does it change anything on laredoute.fr, or only read data?

It only reads. It looks things up on laredoute.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/laredoute.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/laredoute.fr/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/laredoute.fr/get-product
