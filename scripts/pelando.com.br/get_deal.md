# Get Pelando deal

Automatically get Pelando deal on pelando.com.br. Read one deal or coupon posted on Pelando (Brazil's deal community), from its link or slug: title, type (promotion or coupon), temperature (the community vote score in degrees), price in reais, discount, free shipping, voucher code, merchant and the merchant page it links to, communities, the full description as text, image, who posted it, comment count, publication date, and whether it is expired. The fields have the same names as the Dealabs, mydealz and hotukdeals scripts; fields Pelando does not show (previous price, shipping price, start and end dates) are null. An older expired deal is shown by Pelando without its details: then only its id, title, type, status, merchant, image, author, comment count and date are given, and the other fields are null. A deal that does not exist fails with an error that says so.

- Site: pelando.com.br
- Address: `reduck/pelando.com.br/get_deal`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/pelando.com.br/get_deal`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/pelando.com.br/get_deal
```

## Input

- `deal` (string, required): The deal's Pelando link (https://www.pelando.com.br/d/...), or its slug as List Pelando hot deals and Search Pelando deals return it.

## Output

- `id` (string, required)
- `url` (string, required)
- `slug` (string, required)
- `title` (string, required)
- `images` (array, required)
- `categories` (array, required): The Pelando communities the deal is posted in.
- `type` (string, optional): promotion or coupon, as Pelando names it.
- `price` (number | null, optional): Price in reais.
- `is_hot` (boolean | null, optional): Always null: Pelando does not mark deals as hot.
- `status` (string | null, optional): active or expired, as Pelando names it.
- `category` (string | null, optional): The first community of the deal, or null.
- `end_date` (string | null, optional)
- `is_local` (boolean | null, optional): Always null: Pelando does not mark local deals.
- `merchant` (string | null, optional)
- `image_url` (string | null, optional)
- `link_host` (string | null, optional): Domain of the merchant page the deal links to.
- `posted_by` (string | null, optional)
- `is_expired` (boolean, optional)
- `source_url` (string | null, optional): The merchant page the deal links to.
- `start_date` (string | null, optional)
- `description` (string | null, optional): The full description, as text.
- `merchant_id` (string | null, optional)
- `temperature` (number | null, optional): Community vote score in degrees.
- `published_at` (string | null, optional)
- `voucher_code` (string | null, optional)
- `comment_count` (number | null, optional)
- `free_shipping` (boolean | null, optional)
- `shipping_price` (number | null, optional)
- `discount_amount` (number | null, optional): Discount in reais, mostly for coupons.
- `next_best_price` (number | null, optional): Always null: Pelando shows no previous price.
- `discount_percent` (number | null, optional)

## FAQ

### What does "Get Pelando deal" do?

Read one deal or coupon posted on Pelando (Brazil's deal community), from its link or slug: title, type (promotion or coupon), temperature (the community vote score in degrees), price in reais, discount, free shipping, voucher code, merchant and the merchant page it links to, communities, the full description as text, image, who posted it, comment count, publication date, and whether it is expired. The fields have the same names as the Dealabs, mydealz and hotukdeals scripts; fields Pelando does not show (previous price, shipping price, start and end dates) are null. An older expired deal is shown by Pelando without its details: then only its id, title, type, status, merchant, image, author, comment count and date are given, and the other fields are null. A deal that does not exist fails with an error that says so.

### How do I automatically get Pelando deal on pelando.com.br?

Ask an AI agent connected to Reduck to run reduck/pelando.com.br/get_deal, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pelando.com.br/get_deal

### Is there a pelando.com.br API to get Pelando deal?

You do not need one. "Get Pelando deal" drives the real pelando.com.br pages in a browser, so it works whether or not pelando.com.br offers an API for this.

### What information do I need to provide?

Required: deal.

### What does it return?

It returns id, url, slug, type, price, title, images, is_hot, status, category, end_date, is_local, merchant, image_url, link_host, posted_by, categories, is_expired, source_url, start_date, description, merchant_id, temperature, published_at, voucher_code, comment_count, free_shipping, shipping_price, discount_amount, next_best_price, discount_percent.

### Do I need to be logged in to pelando.com.br?

No. It only uses pages of pelando.com.br that are reachable without signing in.

### Does it change anything on pelando.com.br, or only read data?

It only reads. It looks things up on pelando.com.br and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/pelando.com.br/get_deal, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pelando.com.br/get_deal

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/pelando.com.br/get_deal
