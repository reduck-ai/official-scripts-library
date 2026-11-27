# Get Pepper.pl deal

Automatically get Pepper.pl deal on pepper.pl. Read one deal or voucher posted on Pepper.pl (Poland's deal community), from its link or id: title, type, temperature (the community vote), price and previous price in złoty, discount, shipping, voucher code, merchant and the domain it links to, category path, the full description as text, every image, who posted it, comment count, dates, and whether it is expired or local. A deal that does not exist fails with an error that says so; an expired deal is returned with is_expired true.

- Site: pepper.pl
- Address: `reduck/pepper.pl/get_deal`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/pepper.pl/get_deal`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/pepper.pl/get_deal
```

## Input

- `deal` (string, required): The deal's Pepper.pl link, or its id as List Pepper.pl hot deals and Search Pepper.pl deals return it.

## Output

- `id` (string, required)
- `title` (string, required)
- `url` (string | null, optional)
- `type` (string, optional): Deal, Voucher or another thread type, as Pepper.pl names it.
- `price` (number | null, optional)
- `images` (array, optional)
- `is_hot` (boolean, optional)
- `status` (string | null, optional)
- `category` (string | null, optional)
- `end_date` (string | null, optional)
- `is_local` (boolean, optional)
- `merchant` (string | null, optional)
- `image_url` (string | null, optional)
- `link_host` (string | null, optional): Domain of the merchant page the deal links to.
- `posted_by` (string | null, optional)
- `categories` (array, optional): The category path, broadest first.
- `is_expired` (boolean, optional)
- `start_date` (string | null, optional)
- `description` (string | null, optional): The full description, as text.
- `merchant_id` (string | null, optional)
- `temperature` (number | null, optional): Community vote in degrees.
- `published_at` (string | null, optional)
- `voucher_code` (string | null, optional)
- `comment_count` (number | null, optional)
- `free_shipping` (boolean | null, optional)
- `shipping_price` (number | null, optional)
- `next_best_price` (number | null, optional): The price the deal compares to, when the poster gave one.
- `discount_percent` (number | null, optional)

## FAQ

### What does "Get Pepper.pl deal" do?

Read one deal or voucher posted on Pepper.pl (Poland's deal community), from its link or id: title, type, temperature (the community vote), price and previous price in złoty, discount, shipping, voucher code, merchant and the domain it links to, category path, the full description as text, every image, who posted it, comment count, dates, and whether it is expired or local. A deal that does not exist fails with an error that says so; an expired deal is returned with is_expired true.

### How do I automatically get Pepper.pl deal on pepper.pl?

Ask an AI agent connected to Reduck to run reduck/pepper.pl/get_deal, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pepper.pl/get_deal

### Is there a pepper.pl API to get Pepper.pl deal?

You do not need one. "Get Pepper.pl deal" drives the real pepper.pl pages in a browser, so it works whether or not pepper.pl offers an API for this.

### What information do I need to provide?

Required: deal.

### What does it return?

It returns id, url, type, price, title, images, is_hot, status, category, end_date, is_local, merchant, image_url, link_host, posted_by, categories, is_expired, start_date, description, merchant_id, temperature, published_at, voucher_code, comment_count, free_shipping, shipping_price, next_best_price, discount_percent.

### Do I need to be logged in to pepper.pl?

No. It only uses pages of pepper.pl that are reachable without signing in.

### Does it change anything on pepper.pl, or only read data?

It only reads. It looks things up on pepper.pl and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/pepper.pl/get_deal, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pepper.pl/get_deal

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/pepper.pl/get_deal
