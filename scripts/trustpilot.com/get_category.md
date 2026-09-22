# Get Trustpilot category companies

Automatically get Trustpilot category companies on trustpilot.com. List one page of companies ranked in a Trustpilot category (categoryId from get_categories). Supports the site's own filters as args: page, sort (recommended/reviews_count/latest_review), country, trustscore (3.0/4.0/4.5), claimed. Returns each company's domain, TrustScore, stars, review count, location, contact, categories.

- Site: trustpilot.com
- Address: `reduck/trustpilot.com/get_category`
- Updated: 2026-08-14 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/trustpilot.com/get_category`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/trustpilot.com/get_category
```

## Input

- `category` (string, required): categoryId, e.g. "cats_dogs" (from get_categories).
- `page` (integer, optional): 1-based page; 20 companies per page.
- `sort` (any, optional): recommended = Most relevant; reviews_count = Highest number of reviews; latest_review = Most recent reviews.
- `claimed` (boolean, optional): Only companies with a claimed profile.
- `country` (string, optional): ISO-3166 alpha-2 country code, e.g. "US", "GB". Defaults to the viewer locale (US).
- `trustscore` (any, optional): Minimum TrustScore filter (the site's Rating chip: 3+, 4+, 4.5+). Must carry the decimal.

## Output

- `category` (string | null, required)
- `companies` (array, required)
- `totalHits` (integer | null, required)
- `page` (integer | null, optional)
- `perPage` (integer | null, optional)
- `selected` (object | null, optional): Filters the server actually applied (echoed back).
- `totalPages` (integer | null, optional)

## FAQ

### What does "Get Trustpilot category companies" do?

List one page of companies ranked in a Trustpilot category (categoryId from get_categories). Supports the site's own filters as args: page, sort (recommended/reviews_count/latest_review), country, trustscore (3.0/4.0/4.5), claimed. Returns each company's domain, TrustScore, stars, review count, location, contact, categories.

### How do I automatically get Trustpilot category companies on trustpilot.com?

Ask an AI agent connected to Reduck to run reduck/trustpilot.com/get_category, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/trustpilot.com/get_category

### Is there a trustpilot.com API to get Trustpilot category companies?

You do not need one. "Get Trustpilot category companies" drives the real trustpilot.com pages in a browser, so it works whether or not trustpilot.com offers an API for this.

### What information do I need to provide?

Required: category. Optional: page, sort, claimed, country, trustscore.

### What does it return?

It returns page, perPage, category, selected, companies, totalHits, totalPages.

### Do I need to be logged in to trustpilot.com?

No. It only uses pages of trustpilot.com that are reachable without signing in.

### Does it change anything on trustpilot.com, or only read data?

Unknown: its author has not declared whether it changes anything on trustpilot.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/trustpilot.com/get_category, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/trustpilot.com/get_category

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/trustpilot.com/get_category
