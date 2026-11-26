# Get Fnac product

Automatically get Fnac product on fnac.com. Read one fnac.com product from its Fnac id or product page link: title, price, list price, availability, rating, review count, brand, images and seller.

- Site: fnac.com
- Address: `reduck/fnac.com/get-product`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/fnac.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/fnac.com/get-product
```

## Input

- `product` (string, required): Fnac product id as Search Fnac products returns it, for example a23482261 or mp51563287, or a www.fnac.com product page link.

## Output

- `id` (string, required)
- `url` (string, required)
- `price` (number | null, required): Price in euros of the offer shown first.
- `title` (string | null, required)
- `images` (array, required)
- `offers` (array, required): Offers listed on the page, the one shown first included.
- `rating` (number | null, required): Average stars out of 5, null when there are no reviews.
- `seller` (object | null, required)
- `attributes` (array, required): Technical characteristics, in page order. Several values of one characteristic are joined with commas.
- `breadcrumb` (array, required)
- `list_price` (number | null, required): Struck-through reference price in euros, null when none is shown.
- `availability` (string | null, required): schema.org availability the page declares, for example InStock or LimitedAvailability.
- `requested_id` (string, required)
- `review_count` (integer | null, required): Null when there are no reviews.
- `ean` (string | null, optional)
- `mpn` (string | null, optional): Manufacturer reference.
- `brand` (string | null, optional)
- `category` (string | null, optional)
- `condition` (string | null, optional): Condition code of the offer shown, for example new.
- `image_url` (string | null, optional)
- `description` (string | null, optional)
- `shipping_price` (number | null, optional): Shipping price in euros of the offer shown, 0 when free.
- `availability_text` (string | null, optional): Availability as Fnac writes it, in French.

## FAQ

### What does "Get Fnac product" do?

Read one fnac.com product from its Fnac id or product page link: title, price, list price, availability, rating, review count, brand, images and seller.

### How do I automatically get Fnac product on fnac.com?

Ask an AI agent connected to Reduck to run reduck/fnac.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/fnac.com/get-product

### Is there a fnac.com API to get Fnac product?

You do not need one. "Get Fnac product" drives the real fnac.com pages in a browser, so it works whether or not fnac.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns id, ean, mpn, url, brand, price, title, images, offers, rating, seller, category, condition, image_url, attributes, breadcrumb, list_price, description, availability, requested_id, review_count, shipping_price, availability_text.

### Do I need to be logged in to fnac.com?

No. It only uses pages of fnac.com that are reachable without signing in.

### Does it change anything on fnac.com, or only read data?

It only reads. It looks things up on fnac.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/fnac.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/fnac.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/fnac.com/get-product
