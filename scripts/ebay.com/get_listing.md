# Get eBay listing details

Automatically get eBay listing details on ebay.com. Fetch an eBay item listing: title, price, currency, images, condition, brand, seller name, feedback score, and positive-feedback percentage. No login required.

- Site: ebay.com
- Address: `reduck/ebay.com/get_listing`
- Updated: 2026-09-03 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ebay.com/get_listing`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ebay.com/get_listing
```

## Input

- `item_id` (string, required): eBay item id (numeric), e.g. "257563225118" from ebay.com/itm/257563225118

## Output

- `item_id` (string, required)
- `available` (boolean, required)
- `brand` (string | null, optional)
- `color` (string | null, optional)
- `price` (number | null, optional)
- `title` (string | null, optional)
- `currency` (string | null, optional)
- `condition` (string | null, optional)
- `imageUrls` (array, optional)
- `sellerName` (string | null, optional)
- `availability` (string | null, optional)
- `conditionNote` (string | null, optional)
- `sellerFeedbackCount` (integer | null, optional)
- `sellerPositivePercent` (number | null, optional)

## FAQ

### What does "Get eBay listing details" do?

Fetch an eBay item listing: title, price, currency, images, condition, brand, seller name, feedback score, and positive-feedback percentage. No login required.

### How do I automatically get eBay listing details on ebay.com?

Ask an AI agent connected to Reduck to run reduck/ebay.com/get_listing, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ebay.com/get_listing

### Is there a ebay.com API to get eBay listing details?

You do not need one. "Get eBay listing details" drives the real ebay.com pages in a browser, so it works whether or not ebay.com offers an API for this.

### What information do I need to provide?

Required: item_id.

### What does it return?

It returns brand, color, price, title, item_id, currency, available, condition, imageUrls, sellerName, availability, conditionNote, sellerFeedbackCount, sellerPositivePercent.

### Do I need to be logged in to ebay.com?

No. It only uses pages of ebay.com that are reachable without signing in.

### Does it change anything on ebay.com, or only read data?

It only reads. It looks things up on ebay.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ebay.com/get_listing, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ebay.com/get_listing

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/ebay.com/get_listing
