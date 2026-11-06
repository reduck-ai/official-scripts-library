# Get Leboncoin ad details

Automatically get Leboncoin ad details on leboncoin.fr. Read one Leboncoin ad by its link or id: title, full description, price, category, condition and other attributes, place, publication date and the full-size photo links. An ad that is removed or not found returns an error. Opening an ad does not contact the seller.

- Site: leboncoin.fr
- Address: `reduck/leboncoin.fr/get_ad_details`
- Updated: 2026-11-05 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/leboncoin.fr/get_ad_details`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/get_ad_details
```

## Input

- `ad` (string, required): Ad link from list_my_ads or the numeric ad id.

## Output

- `id` (string, required)
- `url` (string, required)
- `photos` (array, required)
- `attributes` (array, required)
- `city` (string | null, optional)
- `price` (number | null, optional)
- `title` (string | null, optional)
- `zipcode` (string | null, optional)
- `category` (string | null, optional)
- `condition` (string | null, optional)
- `description` (string | null, optional)
- `publishedAt` (string | null, optional)

## FAQ

### What does "Get Leboncoin ad details" do?

Read one Leboncoin ad by its link or id: title, full description, price, category, condition and other attributes, place, publication date and the full-size photo links. An ad that is removed or not found returns an error. Opening an ad does not contact the seller.

### How do I automatically get Leboncoin ad details on leboncoin.fr?

Ask an AI agent connected to Reduck to run reduck/leboncoin.fr/get_ad_details, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/get_ad_details

### Is there a leboncoin.fr API to get Leboncoin ad details?

You do not need one. "Get Leboncoin ad details" drives the real leboncoin.fr pages in a browser, so it works whether or not leboncoin.fr offers an API for this.

### What information do I need to provide?

Required: ad.

### What does it return?

It returns id, url, city, price, title, photos, zipcode, category, condition, attributes, description, publishedAt.

### Do I need to be logged in to leboncoin.fr?

No. It only uses pages of leboncoin.fr that are reachable without signing in.

### Does it change anything on leboncoin.fr, or only read data?

It only reads. It looks things up on leboncoin.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/leboncoin.fr/get_ad_details, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/get_ad_details

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/leboncoin.fr/get_ad_details
