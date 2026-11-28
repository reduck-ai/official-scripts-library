# Get Galeries Lafayette product offers

Automatically get Galeries Lafayette product offers on galerieslafayette.com. List the sellers' offers for one size of a galerieslafayette.com product: price, shipping, stock and lead time.

- Site: galerieslafayette.com
- Address: `reduck/galerieslafayette.com/get-product-offers`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/galerieslafayette.com/get-product-offers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/galerieslafayette.com/get-product-offers
```

## Input

- `product` (string, required): A galerieslafayette.com product link or a code from search-products or get-product.
- `size` (string, optional): The size, as get-product lists it (e.g. "M"). Needed when the colour comes in several sizes.

## Output

- `id` (string, required)
- `offers` (array, required): Best offer first, as the site ranks them. Galeries Lafayette's own stock is one offer with offer_id null.
- `variant` (object, required)
- `offers_count` (integer, required)
- `name` (string | null, optional)

## FAQ

### What does "Get Galeries Lafayette product offers" do?

List the sellers' offers for one size of a galerieslafayette.com product: price, shipping, stock and lead time.

### How do I automatically get Galeries Lafayette product offers on galerieslafayette.com?

Ask an AI agent connected to Reduck to run reduck/galerieslafayette.com/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/galerieslafayette.com/get-product-offers

### Is there a galerieslafayette.com API to get Galeries Lafayette product offers?

You do not need one. "Get Galeries Lafayette product offers" drives the real galerieslafayette.com pages in a browser, so it works whether or not galerieslafayette.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: size.

### What does it return?

It returns id, name, offers, variant, offers_count.

### Do I need to be logged in to galerieslafayette.com?

No. It only uses pages of galerieslafayette.com that are reachable without signing in.

### Does it change anything on galerieslafayette.com, or only read data?

It only reads. It looks things up on galerieslafayette.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/galerieslafayette.com/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/galerieslafayette.com/get-product-offers

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/galerieslafayette.com/get-product-offers
