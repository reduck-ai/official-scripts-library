# Get an Amazon.com.br deal

Automatically get an Amazon.com.br deal on amazon.com.br. Read one deal on Amazon.com.br by its deal id (the 8-character id in an amazon.com.br/deal/<id> link, or deal_id from list_deals): the deal's type, state, label as Amazon writes it, discount badge, end time and percent claimed, plus every product in it with ASIN, title, URL, image, deal price and list price with their labels, rating, review count and brand. A deal that Amazon shows no product for is refused.

- Site: amazon.com.br
- Address: `reduck/amazon.com.br/get_deal`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.com.br/get_deal`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.com.br/get_deal
```

## Input

- `dealId` (string, required): The deal id: 8 hex characters, from an amazon.com.br/deal/<id> link or deal_id in list_deals.

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

### What does "Get an Amazon.com.br deal" do?

Read one deal on Amazon.com.br by its deal id (the 8-character id in an amazon.com.br/deal/<id> link, or deal_id from list_deals): the deal's type, state, label as Amazon writes it, discount badge, end time and percent claimed, plus every product in it with ASIN, title, URL, image, deal price and list price with their labels, rating, review count and brand. A deal that Amazon shows no product for is refused.

### How do I automatically get an Amazon.com.br deal on amazon.com.br?

Ask an AI agent connected to Reduck to run reduck/amazon.com.br/get_deal, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com.br/get_deal

### Is there a amazon.com.br API to get an Amazon.com.br deal?

You do not need one. "Get an Amazon.com.br deal" drives the real amazon.com.br pages in a browser, so it works whether or not amazon.com.br offers an API for this.

### What information do I need to provide?

Required: dealId.

### What does it return?

It returns url, deal_id, ends_at, products, deal_type, deal_label, deal_state, discount_label, percent_claimed.

### Do I need to be logged in to amazon.com.br?

No. It only uses pages of amazon.com.br that are reachable without signing in.

### Does it change anything on amazon.com.br, or only read data?

It only reads. It looks things up on amazon.com.br and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.com.br/get_deal, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com.br/get_deal

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.com.br/get_deal
