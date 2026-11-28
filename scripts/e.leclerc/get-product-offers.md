# Get E.Leclerc product offers

Automatically get E.Leclerc product offers on e.leclerc. List every seller's offer for one e.leclerc product: price, condition, delivery and seller rating.

- Site: e.leclerc
- Address: `reduck/e.leclerc/get-product-offers`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/e.leclerc/get-product-offers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/e.leclerc/get-product-offers
```

## Input

- `product` (string, required): An e.leclerc product link or the product's barcode number (id from search-products).

## Output

- `id` (string, required): EAN
- `name` (string | null, required)
- `offers` (array, required): The offer e.leclerc shows first (featured: true), then every other seller's
- `offers_count` (integer, required)

## FAQ

### What does "Get E.Leclerc product offers" do?

List every seller's offer for one e.leclerc product: price, condition, delivery and seller rating.

### How do I automatically get E.Leclerc product offers on e.leclerc?

Ask an AI agent connected to Reduck to run reduck/e.leclerc/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/e.leclerc/get-product-offers

### Is there a e.leclerc API to get E.Leclerc product offers?

You do not need one. "Get E.Leclerc product offers" drives the real e.leclerc pages in a browser, so it works whether or not e.leclerc offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns id, name, offers, offers_count.

### Do I need to be logged in to e.leclerc?

No. It only uses pages of e.leclerc that are reachable without signing in.

### Does it change anything on e.leclerc, or only read data?

It only reads. It looks things up on e.leclerc and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/e.leclerc/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/e.leclerc/get-product-offers

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/e.leclerc/get-product-offers
