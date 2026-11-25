# Get an Amazon.de deal

Automatically get an Amazon.de deal on amazon.de. Get one Amazon.de deal by its id (deal_id from List Amazon.de deals or Get Amazon.de product): its type (LIGHTNING_DEAL, BEST_DEAL, TOP_DEAL), state, discount badge and deal label as Amazon writes them, end time when it counts down, percent claimed for lightning deals, and every product the deal covers, each with ASIN, title, URL, image, deal price and list price in euros, rating and review count. A deal that has ended or does not exist is refused with a message that says so.

- Site: amazon.de
- Address: `reduck/amazon.de/get_deal`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.de/get_deal`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.de/get_deal
```

## Input

- `dealId` (string, required): The deal id, 8 hexadecimal characters, as deal_id in List Amazon.de deals.
- `zipCode` (string, optional): German postcode prices and availability are shown for. Default 10115.

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

### What does "Get an Amazon.de deal" do?

Get one Amazon.de deal by its id (deal_id from List Amazon.de deals or Get Amazon.de product): its type (LIGHTNING_DEAL, BEST_DEAL, TOP_DEAL), state, discount badge and deal label as Amazon writes them, end time when it counts down, percent claimed for lightning deals, and every product the deal covers, each with ASIN, title, URL, image, deal price and list price in euros, rating and review count. A deal that has ended or does not exist is refused with a message that says so.

### How do I automatically get an Amazon.de deal on amazon.de?

Ask an AI agent connected to Reduck to run reduck/amazon.de/get_deal, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.de/get_deal

### Is there a amazon.de API to get an Amazon.de deal?

You do not need one. "Get an Amazon.de deal" drives the real amazon.de pages in a browser, so it works whether or not amazon.de offers an API for this.

### What information do I need to provide?

Required: dealId. Optional: zipCode.

### What does it return?

It returns url, deal_id, ends_at, products, deal_type, deal_label, deal_state, discount_label, percent_claimed.

### Do I need to be logged in to amazon.de?

No. It only uses pages of amazon.de that are reachable without signing in.

### Does it change anything on amazon.de, or only read data?

It only reads. It looks things up on amazon.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.de/get_deal, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.de/get_deal

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.de/get_deal
