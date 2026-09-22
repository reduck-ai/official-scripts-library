# Get Yelp business photos

Automatically get Yelp business photos on yelp.com. List photos for a Yelp business by slug, with captions and category counts (Food/Inside/Outside/Menu/Drink/Videos). Returns the first batch of photos as loaded by Yelp's photo page.

- Site: yelp.com
- Address: `reduck/yelp.com/get_business_photos`
- Updated: 2026-08-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/yelp.com/get_business_photos`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/yelp.com/get_business_photos
```

## Input

- `slug` (string, required): Yelp business slug, e.g. 'l-industrie-pizzeria-new-york'

## Output

- `slug` (string, optional)
- `count` (integer, optional)
- `total` (integer | null, optional)
- `photos` (array, optional)
- `categories` (object, optional)

## FAQ

### What does "Get Yelp business photos" do?

List photos for a Yelp business by slug, with captions and category counts (Food/Inside/Outside/Menu/Drink/Videos). Returns the first batch of photos as loaded by Yelp's photo page.

### How do I automatically get Yelp business photos on yelp.com?

Ask an AI agent connected to Reduck to run reduck/yelp.com/get_business_photos, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/yelp.com/get_business_photos

### Is there a yelp.com API to get Yelp business photos?

You do not need one. "Get Yelp business photos" drives the real yelp.com pages in a browser, so it works whether or not yelp.com offers an API for this.

### What information do I need to provide?

Required: slug.

### What does it return?

It returns slug, count, total, photos, categories.

### Do I need to be logged in to yelp.com?

No. It only uses pages of yelp.com that are reachable without signing in.

### Does it change anything on yelp.com, or only read data?

It only reads. It looks things up on yelp.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/yelp.com/get_business_photos, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/yelp.com/get_business_photos

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/yelp.com/get_business_photos
