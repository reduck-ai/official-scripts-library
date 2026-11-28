# Get E.Leclerc product

Automatically get E.Leclerc product on e.leclerc. Read one e.leclerc product by its link or barcode number.

- Site: e.leclerc
- Address: `reduck/e.leclerc/get-product`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/e.leclerc/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/e.leclerc/get-product
```

## Input

- `product` (string, required): An e.leclerc product link (https://www.e.leclerc/fp/...) or the product's barcode number, as search-products returns in id.

## Output

- `id` (string, required)
- `url` (string, required)
- `name` (string | null, required)
- `price` (number | null, required)
- `currency` (string, required)
- `brand` (string | null, optional)
- `specs` (object, optional): Labelled product facts, e.g. Marque, Nombre de pièces
- `seller` (string | null, optional)
- `category` (string | null, optional)
- `in_stock` (boolean, optional)
- `offer_id` (string | null, optional)
- `image_url` (string | null, optional)
- `image_urls` (array, optional)
- `list_price` (number | null, optional)
- `description` (string | null, optional)
- `offers_count` (integer, optional)

## FAQ

### What does "Get E.Leclerc product" do?

Read one e.leclerc product by its link or barcode number.

### How do I automatically get E.Leclerc product on e.leclerc?

Ask an AI agent connected to Reduck to run reduck/e.leclerc/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/e.leclerc/get-product

### Is there a e.leclerc API to get E.Leclerc product?

You do not need one. "Get E.Leclerc product" drives the real e.leclerc pages in a browser, so it works whether or not e.leclerc offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns id, url, name, brand, price, specs, seller, category, currency, in_stock, offer_id, image_url, image_urls, list_price, description, offers_count.

### Do I need to be logged in to e.leclerc?

No. It only uses pages of e.leclerc that are reachable without signing in.

### Does it change anything on e.leclerc, or only read data?

It only reads. It looks things up on e.leclerc and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/e.leclerc/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/e.leclerc/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/e.leclerc/get-product
