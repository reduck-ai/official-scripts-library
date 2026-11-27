# Get a Lenovo product

Automatically get a Lenovo product on lenovo.com. Get one product of the Lenovo US store (lenovo.com/us/en) by its product link or its product code (for example 83CQ003BUS, as given by Search Lenovo products). Returns the product code, name, link, brand, series code, price, list price and saving in US dollars, availability, condition, badges, images and the technical specifications as name and value pairs. The product code identifies a fixed, pre-built model: it is the code a cart takes. Configurable models are read as their page shows them by default. An unknown code or a link that is not a Lenovo US product page fails with an error that says so. When Lenovo shows its "Access Denied" page, the run fails and says so.

- Site: lenovo.com
- Address: `reduck/lenovo.com/get-product`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/lenovo.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/lenovo.com/get-product
```

## Input

- `url` (string, optional): Lenovo US product link (https://www.lenovo.com/us/en/p/...), as given by Search Lenovo products.
- `product_code` (string, optional): Lenovo product code, for example 83CQ003BUS. Used when no url is given.

## Output

- `url` (string, required)
- `name` (string | null, required)
- `brand` (string | null, required)
- `price` (number | null, required): Price now, in the currency field (US dollars).
- `specs` (array | null, required): Technical specifications. Null when the page loaded none.
- `badges` (array, required): Labels the page shows on the product, for example DOORBUSTER.
- `saving` (number | null, required)
- `currency` (string | null, required)
- `condition` (string | null, required)
- `was_price` (number | null, required): Lenovo's list price before the saving.
- `image_urls` (array, required)
- `series_code` (string | null, required): Lenovo's code of the product series.
- `availability` (string | null, required): Availability as the page gives it, for example InStock or OutOfStock.
- `product_code` (string, required)

## FAQ

### What does "Get a Lenovo product" do?

Get one product of the Lenovo US store (lenovo.com/us/en) by its product link or its product code (for example 83CQ003BUS, as given by Search Lenovo products). Returns the product code, name, link, brand, series code, price, list price and saving in US dollars, availability, condition, badges, images and the technical specifications as name and value pairs. The product code identifies a fixed, pre-built model: it is the code a cart takes. Configurable models are read as their page shows them by default. An unknown code or a link that is not a Lenovo US product page fails with an error that says so. When Lenovo shows its "Access Denied" page, the run fails and says so.

### How do I automatically get a Lenovo product on lenovo.com?

Ask an AI agent connected to Reduck to run reduck/lenovo.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lenovo.com/get-product

### Is there a lenovo.com API to get a Lenovo product?

You do not need one. "Get a Lenovo product" drives the real lenovo.com pages in a browser, so it works whether or not lenovo.com offers an API for this.

### What information do I need to provide?

Optional: url, product_code.

### What does it return?

It returns url, name, brand, price, specs, badges, saving, currency, condition, was_price, image_urls, series_code, availability, product_code.

### Do I need to be logged in to lenovo.com?

No. It only uses pages of lenovo.com that are reachable without signing in.

### Does it change anything on lenovo.com, or only read data?

It only reads. It looks things up on lenovo.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/lenovo.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lenovo.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/lenovo.com/get-product
