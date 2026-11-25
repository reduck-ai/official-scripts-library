# Get Alza.cz product

Automatically get Alza.cz product on alza.cz. Read an Alza.cz product page from its link: id, code, name, brand, price in Czech crowns, availability, description, rating and main image. A link that is not an Alza product page fails with an error; a product page that no longer exists fails with an error.

- Site: alza.cz
- Address: `reduck/alza.cz/get-product`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/alza.cz/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/alza.cz/get-product
```

## Input

- `url` (string, required): Link of an Alza.cz product page, as Search Alza.cz products gives it, for example https://www.alza.cz/gp-nabijecka-baterii-recyko-b423-4-aa-recyko-2100-mah-d13308667.htm.

## Output

- `url` (string, required)
- `code` (string | null, required): Alza product code.
- `name` (string | null, required)
- `brand` (string | null, required)
- `price` (number | null, required): Current price in Czech crowns, taxes included.
- `currency` (string | null, required)
- `imageUrl` (string | null, required)
- `productId` (string, required)
- `description` (string | null, required)
- `ratingCount` (integer | null, required)
- `ratingValue` (number | null, required)
- `availability` (string | null, required): Availability as the site declares it, for example InStock.

## FAQ

### What does "Get Alza.cz product" do?

Read an Alza.cz product page from its link: id, code, name, brand, price in Czech crowns, availability, description, rating and main image. A link that is not an Alza product page fails with an error; a product page that no longer exists fails with an error.

### How do I automatically get Alza.cz product on alza.cz?

Ask an AI agent connected to Reduck to run reduck/alza.cz/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/alza.cz/get-product

### Is there a alza.cz API to get Alza.cz product?

You do not need one. "Get Alza.cz product" drives the real alza.cz pages in a browser, so it works whether or not alza.cz offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns url, code, name, brand, price, currency, imageUrl, productId, description, ratingCount, ratingValue, availability.

### Do I need to be logged in to alza.cz?

No. It only uses pages of alza.cz that are reachable without signing in.

### Does it change anything on alza.cz, or only read data?

It only reads. It looks things up on alza.cz and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/alza.cz/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/alza.cz/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/alza.cz/get-product
