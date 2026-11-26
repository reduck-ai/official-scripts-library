# Get a Dell product

Automatically get a Dell product on dell.com. Read one product of the Dell US store by its id or link: name, price, list price, availability, rating, images and configurations.

- Site: dell.com
- Address: `reduck/dell.com/get-product`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dell.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dell.com/get-product
```

## Input

- `product` (string, required): Product id (e.g. "se2426h" or "dx13260_so_42") or the link of a Dell US product page.

## Output

- `id` (string, required)
- `url` (string, required)
- `name` (string | null, required)
- `mpn` (string | null, optional)
- `sku` (string | null, optional)
- `gtin` (string | null, optional)
- `brand` (string | null, optional)
- `model` (string | null, optional)
- `price` (number | null, optional): Dell price in USD.
- `images` (array, optional)
- `rating` (number | null, optional)
- `seller` (string | null, optional)
- `currency` (string, optional)
- `variants` (array, optional): Other configurations or colors of the same model, each with its own product id.
- `list_price` (number | null, optional): Price before discount (estimated value) in USD.
- `description` (string | null, optional)
- `availability` (string | null, optional): Stock status as the page gives it, e.g. instock, or available / unavailable from its Add to Cart button.
- `review_count` (integer | null, optional)

## FAQ

### What does "Get a Dell product" do?

Read one product of the Dell US store by its id or link: name, price, list price, availability, rating, images and configurations.

### How do I automatically get a Dell product on dell.com?

Ask an AI agent connected to Reduck to run reduck/dell.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dell.com/get-product

### Is there a dell.com API to get a Dell product?

You do not need one. "Get a Dell product" drives the real dell.com pages in a browser, so it works whether or not dell.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns id, mpn, sku, url, gtin, name, brand, model, price, images, rating, seller, currency, variants, list_price, description, availability, review_count.

### Do I need to be logged in to dell.com?

No. It only uses pages of dell.com that are reachable without signing in.

### Does it change anything on dell.com, or only read data?

It only reads. It looks things up on dell.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dell.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dell.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/dell.com/get-product
