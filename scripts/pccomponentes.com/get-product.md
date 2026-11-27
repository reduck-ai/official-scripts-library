# Get PcComponentes product

Automatically get PcComponentes product on pccomponentes.com. Fetch one PcComponentes Spain (pccomponentes.com) product page by its link (the url of Search PcComponentes products, or the slug of that link). Returns article number, title, brand, barcode number, manufacturer reference, family, condition, price and struck-through price in euros with what that price is, rating out of 5 and review count, whether it can be bought, the delivery window, main image and all images, description as plain text, category path, the product's attributes, and every offer of the product (PcComponentes and marketplace sellers, each with price, condition, shipping cost and stock). Texts are in Spanish. A link that opens no product fails with an error that says so.

- Site: pccomponentes.com
- Address: `reduck/pccomponentes.com/get-product`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/pccomponentes.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/pccomponentes.com/get-product
```

## Input

- `product` (string, required): Product link (the url of Search PcComponentes products), or the slug at the end of that link.

## Output

- `url` (string, required)
- `price` (number | null, required): Price in euros, VAT included.
- `title` (string | null, required)
- `offers` (array, required): Every offer of the product, the main one first. Empty when the page lists none.
- `requested` (string, required)
- `product_id` (string, required): PcComponentes article number.
- `ean` (string | null, optional)
- `mpn` (string | null, optional): Manufacturer reference.
- `brand` (string | null, optional)
- `images` (array, optional)
- `rating` (number | null, optional): Average rating out of 5. Null when nobody rated the product.
- `category` (string | null, optional)
- `condition` (string | null, optional): new, or the condition of a refurbished product.
- `image_url` (string | null, optional)
- `breadcrumb` (array, optional)
- `list_price` (number | null, optional): Struck-through price in euros, null when none is shown.
- `description` (string | null, optional)
- `purchasable` (boolean | null, optional)
- `delivery_max` (string | null, optional): Latest delivery date, YYYY-MM-DD.
- `delivery_min` (string | null, optional): Earliest delivery date, YYYY-MM-DD.
- `review_count` (integer | null, optional)
- `specifications` (array, optional): The product's attributes as the site groups them, in Spanish.
- `list_price_type` (string | null, optional): What list_price is, as the site names it, for example PVPR (recommended retail price).

## FAQ

### What does "Get PcComponentes product" do?

Fetch one PcComponentes Spain (pccomponentes.com) product page by its link (the url of Search PcComponentes products, or the slug of that link). Returns article number, title, brand, barcode number, manufacturer reference, family, condition, price and struck-through price in euros with what that price is, rating out of 5 and review count, whether it can be bought, the delivery window, main image and all images, description as plain text, category path, the product's attributes, and every offer of the product (PcComponentes and marketplace sellers, each with price, condition, shipping cost and stock). Texts are in Spanish. A link that opens no product fails with an error that says so.

### How do I automatically get PcComponentes product on pccomponentes.com?

Ask an AI agent connected to Reduck to run reduck/pccomponentes.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pccomponentes.com/get-product

### Is there a pccomponentes.com API to get PcComponentes product?

You do not need one. "Get PcComponentes product" drives the real pccomponentes.com pages in a browser, so it works whether or not pccomponentes.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns ean, mpn, url, brand, price, title, images, offers, rating, category, condition, image_url, requested, breadcrumb, list_price, product_id, description, purchasable, delivery_max, delivery_min, review_count, specifications, list_price_type.

### Do I need to be logged in to pccomponentes.com?

No. It only uses pages of pccomponentes.com that are reachable without signing in.

### Does it change anything on pccomponentes.com, or only read data?

It only reads. It looks things up on pccomponentes.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/pccomponentes.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pccomponentes.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/pccomponentes.com/get-product
