# Get Carrefour product

Automatically get Carrefour product on carrefour.fr. Read one Carrefour.fr product from its barcode number (as Search Carrefour products returns it) or its product link: title, brand, link, price in euros and unit price of the offer shown, seller, availability, purchase limit, category path, images, description, rating, and how many other offers it has with the best one. An unknown barcode number fails with an error that says so.

- Site: carrefour.fr
- Address: `reduck/carrefour.fr/get-product`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/carrefour.fr/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/carrefour.fr/get-product
```

## Input

- `product` (string, required): Barcode number of the product (8 to 14 digits), or a carrefour.fr/p/... link.

## Output

- `id` (string, required)
- `url` (string, required)
- `price` (number | null, required)
- `title` (string, required)
- `seller` (string, required)
- `available` (boolean, required)
- `brand` (string | null, optional)
- `images` (array, optional)
- `rating` (number | null, optional)
- `category` (array, optional)
- `offer_id` (string | null, optional)
- `description` (string | null, optional)
- `max_quantity` (integer | null, optional)
- `other_offers` (integer, optional)
- `review_count` (integer | null, optional)
- `unit_price_label` (string | null, optional)
- `best_other_offer_price` (number | null, optional)

## FAQ

### What does "Get Carrefour product" do?

Read one Carrefour.fr product from its barcode number (as Search Carrefour products returns it) or its product link: title, brand, link, price in euros and unit price of the offer shown, seller, availability, purchase limit, category path, images, description, rating, and how many other offers it has with the best one. An unknown barcode number fails with an error that says so.

### How do I automatically get Carrefour product on carrefour.fr?

Ask an AI agent connected to Reduck to run reduck/carrefour.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/carrefour.fr/get-product

### Is there a carrefour.fr API to get Carrefour product?

You do not need one. "Get Carrefour product" drives the real carrefour.fr pages in a browser, so it works whether or not carrefour.fr offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns id, url, brand, price, title, images, rating, seller, category, offer_id, available, description, max_quantity, other_offers, review_count, unit_price_label, best_other_offer_price.

### Do I need to be logged in to carrefour.fr?

No. It only uses pages of carrefour.fr that are reachable without signing in.

### Does it change anything on carrefour.fr, or only read data?

It only reads. It looks things up on carrefour.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/carrefour.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/carrefour.fr/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/carrefour.fr/get-product
