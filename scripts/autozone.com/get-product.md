# Get an AutoZone product

Automatically get an AutoZone product on autozone.com. Read one AutoZone product by its id or product link: name, price, stock for ship-to-home and store pickup, rating, images, brand, part number, specifications and features.

- Site: autozone.com
- Address: `reduck/autozone.com/get-product`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/autozone.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/autozone.com/get-product
```

## Input

- `product` (string, required): AutoZone product id (the number at the end of a product link, e.g. 663640, as returned by search-products) or a product link https://www.autozone.com/p/<name>/<id>.

## Output

- `id` (string, required)
- `url` (string | null, required)
- `name` (string | null, required)
- `price` (number | null, required)
- `images` (array, required)
- `currency` (string, required)
- `availability` (object, required)
- `specifications` (array, required)
- `brand` (string | null, optional)
- `rating` (number | null, optional)
- `category` (string | null, optional)
- `features` (array, optional)
- `warranty` (string | null, optional)
- `sub_brand` (string | null, optional)
- `list_price` (number | null, optional): The former price when the site shows one, else null.
- `breadcrumbs` (array, optional)
- `description` (string | null, optional)
- `part_number` (string | null, optional)
- `review_count` (integer | null, optional)
- `vehicle_fitment` (string | null, optional): VEHICLE_SPECIFIC or UNIVERSAL, as the site labels it.

## FAQ

### What does "Get an AutoZone product" do?

Read one AutoZone product by its id or product link: name, price, stock for ship-to-home and store pickup, rating, images, brand, part number, specifications and features.

### How do I automatically get an AutoZone product on autozone.com?

Ask an AI agent connected to Reduck to run reduck/autozone.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/autozone.com/get-product

### Is there a autozone.com API to get an AutoZone product?

You do not need one. "Get an AutoZone product" drives the real autozone.com pages in a browser, so it works whether or not autozone.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns id, url, name, brand, price, images, rating, category, currency, features, warranty, sub_brand, list_price, breadcrumbs, description, part_number, availability, review_count, specifications, vehicle_fitment.

### Do I need to be logged in to autozone.com?

No. It only uses pages of autozone.com that are reachable without signing in.

### Does it change anything on autozone.com, or only read data?

It only reads. It looks things up on autozone.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/autozone.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/autozone.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/autozone.com/get-product
