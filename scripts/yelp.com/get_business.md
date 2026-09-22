# Get Yelp business profile

Automatically get Yelp business profile on yelp.com. Fetch a Yelp business's full profile by slug or URL: name, rating, review count, categories, price range, address, phone, hours, website, and cuisine.

- Site: yelp.com
- Address: `reduck/yelp.com/get_business`
- Updated: 2026-08-14 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/yelp.com/get_business`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/yelp.com/get_business
```

## Input

- `slug` (string, required): Yelp business slug or full URL, e.g. 'l-industrie-pizzeria-new-york' or a yelp.com/biz/... URL

## Output

- `url` (string, optional)
- `name` (string | null, optional)
- `slug` (string, optional)
- `phone` (string | null, optional)
- `rating` (number | null, optional)
- `address` (object | null, optional)
- `cuisine` (string | null, optional)
- `website` (string | null, optional)
- `categories` (array, optional)
- `price_range` (string | null, optional)
- `review_count` (integer | null, optional)
- `opening_hours` (array, optional)

## FAQ

### What does "Get Yelp business profile" do?

Fetch a Yelp business's full profile by slug or URL: name, rating, review count, categories, price range, address, phone, hours, website, and cuisine.

### How do I automatically get Yelp business profile on yelp.com?

Ask an AI agent connected to Reduck to run reduck/yelp.com/get_business, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/yelp.com/get_business

### Is there a yelp.com API to get Yelp business profile?

You do not need one. "Get Yelp business profile" drives the real yelp.com pages in a browser, so it works whether or not yelp.com offers an API for this.

### What information do I need to provide?

Required: slug.

### What does it return?

It returns url, name, slug, phone, rating, address, cuisine, website, categories, price_range, review_count, opening_hours.

### Do I need to be logged in to yelp.com?

No. It only uses pages of yelp.com that are reachable without signing in.

### Does it change anything on yelp.com, or only read data?

It only reads. It looks things up on yelp.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/yelp.com/get_business, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/yelp.com/get_business

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/yelp.com/get_business
