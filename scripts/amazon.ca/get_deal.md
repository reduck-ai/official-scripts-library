# Get an Amazon.ca deal

Automatically get an Amazon.ca deal on amazon.ca. Read one deal on Amazon.ca by its deal id (the 8-character id in an amazon.ca/deal/<id> link, or deal_id from list_deals): the deal's type, state, label as Amazon writes it, discount badge, end time and percent claimed, plus every product in it with ASIN, title, URL, image, deal price and list price with their labels, rating, review count and brand. A deal that Amazon shows no product for is refused.

- Site: amazon.ca
- Address: `reduck/amazon.ca/get_deal`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.ca/get_deal`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.ca/get_deal
```

## Input

- `dealId` (string, required): The deal id: 8 hex characters, from an amazon.ca/deal/<id> link or deal_id in list_deals.

## Output

- `url` (string, required)
- `deal_id` (string, required)
- `products` (array, required)
- `ends_at` (string | null, optional)
- `deal_type` (string | null, optional)
- `deal_label` (string | null, optional)
- `deal_state` (string | null, optional)
- `discount_label` (string | null, optional)
- `percent_claimed` (number | null, optional)

## FAQ

### What does "Get an Amazon.ca deal" do?

Read one deal on Amazon.ca by its deal id (the 8-character id in an amazon.ca/deal/<id> link, or deal_id from list_deals): the deal's type, state, label as Amazon writes it, discount badge, end time and percent claimed, plus every product in it with ASIN, title, URL, image, deal price and list price with their labels, rating, review count and brand. A deal that Amazon shows no product for is refused.

### How do I automatically get an Amazon.ca deal on amazon.ca?

Ask an AI agent connected to Reduck to run reduck/amazon.ca/get_deal, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.ca/get_deal

### Is there a amazon.ca API to get an Amazon.ca deal?

You do not need one. "Get an Amazon.ca deal" drives the real amazon.ca pages in a browser, so it works whether or not amazon.ca offers an API for this.

### What information do I need to provide?

Required: dealId.

### What does it return?

It returns url, deal_id, ends_at, products, deal_type, deal_label, deal_state, discount_label, percent_claimed.

### Do I need to be logged in to amazon.ca?

No. It only uses pages of amazon.ca that are reachable without signing in.

### Does it change anything on amazon.ca, or only read data?

It only reads. It looks things up on amazon.ca and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.ca/get_deal, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.ca/get_deal

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.ca/get_deal
