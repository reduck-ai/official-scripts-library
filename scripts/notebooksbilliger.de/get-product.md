# Get notebooksbilliger.de product

Automatically get notebooksbilliger.de product on notebooksbilliger.de. Read one notebooksbilliger.de product by its link: name, brand, article number, barcode (gtin), manufacturer part number, price and list price in euros, availability, rating, review count, description and image. Takes the link Search notebooksbilliger.de products returns.

- Site: notebooksbilliger.de
- Address: `reduck/notebooksbilliger.de/get-product`
- Updated: 2026-11-27 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/notebooksbilliger.de/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/notebooksbilliger.de/get-product
```

## Input

- `url` (string, required): The product's link as Search notebooksbilliger.de products returns it, ending in +<id>.

## Output

- `id` (string, required)
- `url` (string, required)
- `name` (string | null, required)
- `mpn` (string | null, optional)
- `gtin` (string | null, optional)
- `brand` (string | null, optional)
- `price` (number | null, optional): Price in euros.
- `rating` (number | null, optional)
- `currency` (string | null, optional)
- `image_url` (string | null, optional)
- `list_price` (number | null, optional): List price the page states in euros, when higher than the price.
- `description` (string | null, optional)
- `availability` (string | null, optional): schema.org availability, e.g. InStock.
- `review_count` (integer | null, optional)
- `article_number` (string | null, optional)

## FAQ

### What does "Get notebooksbilliger.de product" do?

Read one notebooksbilliger.de product by its link: name, brand, article number, barcode (gtin), manufacturer part number, price and list price in euros, availability, rating, review count, description and image. Takes the link Search notebooksbilliger.de products returns.

### How do I automatically get notebooksbilliger.de product on notebooksbilliger.de?

Ask an AI agent connected to Reduck to run reduck/notebooksbilliger.de/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/notebooksbilliger.de/get-product

### Is there a notebooksbilliger.de API to get notebooksbilliger.de product?

You do not need one. "Get notebooksbilliger.de product" drives the real notebooksbilliger.de pages in a browser, so it works whether or not notebooksbilliger.de offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns id, mpn, url, gtin, name, brand, price, rating, currency, image_url, list_price, description, availability, review_count, article_number.

### Do I need to be logged in to notebooksbilliger.de?

No. It only uses pages of notebooksbilliger.de that are reachable without signing in.

### Does it change anything on notebooksbilliger.de, or only read data?

It only reads. It looks things up on notebooksbilliger.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/notebooksbilliger.de/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/notebooksbilliger.de/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/notebooksbilliger.de/get-product
