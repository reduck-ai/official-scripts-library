# Get Lowe's product offers

Automatically get Lowe's product offers on lowes.com. List the sellers that offer one Lowes.com product, from its link or item id. Lowe's sells each item through one seller: Lowe's itself, or one seller of the Lowe's Marketplace that sells and ships it. For that offer you get the price and struck-through price in US dollars, the seller name and id, who ships it, the shipping price and the delivery estimate of the shipping method, and whether it can be bought. Page 1 holds the offer; a page past the last one returns no offers. Prices, shipping and dates follow the store and ZIP code Lowe's assigns to the browser's location.

- Site: lowes.com
- Address: `reduck/lowes.com/get-product-offers`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/lowes.com/get-product-offers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/lowes.com/get-product-offers
```

## Input

- `url` (string, optional): Lowe's product page link (https://www.lowes.com/pd/<name>/<id>), as returned by Search Lowe's products.
- `page` (integer, optional): Page of the offer list. Lowe's has one offer per item, so page 1 holds it; has_next_page says when to stop.
- `item_id` (string, optional): Lowe's item id (item_id of Search Lowe's products). Used when no url is given.

## Output

- `url` (string, required)
- `page` (integer, required)
- `offers` (array, required)
- `item_id` (string, required)
- `total_offers` (integer, required): Offers for this item, all pages together.
- `has_next_page` (boolean, required)
- `title` (string | null, optional)
- `zip_code` (string | null, optional): ZIP code that the shipping price and delivery estimate are for.

## FAQ

### What does "Get Lowe's product offers" do?

List the sellers that offer one Lowes.com product, from its link or item id. Lowe's sells each item through one seller: Lowe's itself, or one seller of the Lowe's Marketplace that sells and ships it. For that offer you get the price and struck-through price in US dollars, the seller name and id, who ships it, the shipping price and the delivery estimate of the shipping method, and whether it can be bought. Page 1 holds the offer; a page past the last one returns no offers. Prices, shipping and dates follow the store and ZIP code Lowe's assigns to the browser's location.

### How do I automatically get Lowe's product offers on lowes.com?

Ask an AI agent connected to Reduck to run reduck/lowes.com/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lowes.com/get-product-offers

### Is there a lowes.com API to get Lowe's product offers?

You do not need one. "Get Lowe's product offers" drives the real lowes.com pages in a browser, so it works whether or not lowes.com offers an API for this.

### What information do I need to provide?

Optional: url, page, item_id.

### What does it return?

It returns url, page, title, offers, item_id, zip_code, total_offers, has_next_page.

### Do I need to be logged in to lowes.com?

No. It only uses pages of lowes.com that are reachable without signing in.

### Does it change anything on lowes.com, or only read data?

It only reads. It looks things up on lowes.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/lowes.com/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lowes.com/get-product-offers

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/lowes.com/get-product-offers
