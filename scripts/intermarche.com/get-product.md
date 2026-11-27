# Get Intermarché product

Automatically get Intermarché product on intermarche.com. Read one Intermarché.com product in one store (prices and stock are per store) from its product link, as Search Intermarché products returns it: title, brand, description, price and crossed-out price in euros, unit price, packaging, stock, per-order limit, availability, storage advice, legal information and images. The store is its 5-digit code (for example 09571). A link to no product fails with an error that says so.

- Site: intermarche.com
- Address: `reduck/intermarche.com/get-product`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/intermarche.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/intermarche.com/get-product
```

## Input

- `store` (string, required): Store code, 5 digits, e.g. 09571.
- `product` (string, required): The product's intermarche.com/produit/<name>/<barcode> link, as Search Intermarché products returns it in url.

## Output

- `ean` (string, required)
- `price` (number | null, required)
- `store` (string, required)
- `title` (string | null, required)
- `id` (string | null, optional)
- `url` (string, optional)
- `brand` (string | null, optional)
- `stock` (integer | null, optional)
- `images` (array, optional)
- `storage` (string | null, optional)
- `available` (boolean | null, optional)
- `packaging` (string | null, optional)
- `list_price` (number | null, optional)
- `description` (string | null, optional)
- `max_per_order` (integer | null, optional)
- `unit_price_label` (string | null, optional)
- `legal_information` (string | null, optional)

## FAQ

### What does "Get Intermarché product" do?

Read one Intermarché.com product in one store (prices and stock are per store) from its product link, as Search Intermarché products returns it: title, brand, description, price and crossed-out price in euros, unit price, packaging, stock, per-order limit, availability, storage advice, legal information and images. The store is its 5-digit code (for example 09571). A link to no product fails with an error that says so.

### How do I automatically get Intermarché product on intermarche.com?

Ask an AI agent connected to Reduck to run reduck/intermarche.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/intermarche.com/get-product

### Is there a intermarche.com API to get Intermarché product?

You do not need one. "Get Intermarché product" drives the real intermarche.com pages in a browser, so it works whether or not intermarche.com offers an API for this.

### What information do I need to provide?

Required: product, store.

### What does it return?

It returns id, ean, url, brand, price, stock, store, title, images, storage, available, packaging, list_price, description, max_per_order, unit_price_label, legal_information.

### Do I need to be logged in to intermarche.com?

No. It only uses pages of intermarche.com that are reachable without signing in.

### Does it change anything on intermarche.com, or only read data?

It only reads. It looks things up on intermarche.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/intermarche.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/intermarche.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/intermarche.com/get-product
