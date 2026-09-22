# Get eBay seller storefront details

Automatically get eBay seller storefront details on ebay.com. Fetch an eBay seller's storefront: name, positive feedback percentage, items sold, and follower count. No login required.

- Site: ebay.com
- Address: `reduck/ebay.com/get_seller`
- Updated: 2026-09-03 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ebay.com/get_seller`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ebay.com/get_seller
```

## Input

- `seller_id` (string, required): eBay store/seller username, e.g. "warrantyrepaircenter" from ebay.com/str/warrantyrepaircenter

## Output

- `available` (boolean, required)
- `seller_id` (string, required)
- `name` (string | null, optional)
- `followerCount` (integer | null, optional)
- `itemsSoldText` (string | null, optional)
- `positiveFeedbackPercent` (number | null, optional)

## FAQ

### What does "Get eBay seller storefront details" do?

Fetch an eBay seller's storefront: name, positive feedback percentage, items sold, and follower count. No login required.

### How do I automatically get eBay seller storefront details on ebay.com?

Ask an AI agent connected to Reduck to run reduck/ebay.com/get_seller, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ebay.com/get_seller

### Is there a ebay.com API to get eBay seller storefront details?

You do not need one. "Get eBay seller storefront details" drives the real ebay.com pages in a browser, so it works whether or not ebay.com offers an API for this.

### What information do I need to provide?

Required: seller_id.

### What does it return?

It returns name, available, seller_id, followerCount, itemsSoldText, positiveFeedbackPercent.

### Do I need to be logged in to ebay.com?

No. It only uses pages of ebay.com that are reachable without signing in.

### Does it change anything on ebay.com, or only read data?

It only reads. It looks things up on ebay.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ebay.com/get_seller, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ebay.com/get_seller

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/ebay.com/get_seller
