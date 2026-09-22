# Get Trustpilot company reviews

Automatically get Trustpilot company reviews on trustpilot.com. Get one page (20) of a company's Trustpilot reviews: author, rating, title, text, dates, likes, verification and the company's reply. Supports the site's own filters as args (page, sort, stars, language, keyword search, verified, date range). Defaults to returning reviews in every language so none are silently filtered out by locale.

- Site: trustpilot.com
- Address: `reduck/trustpilot.com/get_reviews`
- Updated: 2026-08-14 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/trustpilot.com/get_reviews`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/trustpilot.com/get_reviews
```

## Input

- `domain` (string, required): Company domain key, e.g. "amazon.com" (identifyingName from search_company).
- `date` (string, optional): Restrict to a recent date range.
- `page` (integer, optional): 1-based page; 20 reviews per page.
- `stars` (array, optional): Filter to these star ratings, e.g. [1] or [4,5].
- `search` (string, optional): Keyword search within this company's reviews.
- `language` (string, optional): ISO code (e.g. "en") or "all". Site default is the viewer locale; "all" returns every language.
- `verified` (boolean, optional): Only verified reviews.

## Output

- `domain` (string, required): Resolved identifyingName.
- `reviews` (array, required)
- `selected` (object, required): Filters the server actually applied (echoed back).
- `pagination` (object, required)

## FAQ

### What does "Get Trustpilot company reviews" do?

Get one page (20) of a company's Trustpilot reviews: author, rating, title, text, dates, likes, verification and the company's reply. Supports the site's own filters as args (page, sort, stars, language, keyword search, verified, date range). Defaults to returning reviews in every language so none are silently filtered out by locale.

### How do I automatically get Trustpilot company reviews on trustpilot.com?

Ask an AI agent connected to Reduck to run reduck/trustpilot.com/get_reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/trustpilot.com/get_reviews

### Is there a trustpilot.com API to get Trustpilot company reviews?

You do not need one. "Get Trustpilot company reviews" drives the real trustpilot.com pages in a browser, so it works whether or not trustpilot.com offers an API for this.

### What information do I need to provide?

Required: domain. Optional: date, page, stars, search, language, verified.

### What does it return?

It returns domain, reviews, selected, pagination.

### Do I need to be logged in to trustpilot.com?

No. It only uses pages of trustpilot.com that are reachable without signing in.

### Does it change anything on trustpilot.com, or only read data?

It only reads. It looks things up on trustpilot.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/trustpilot.com/get_reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/trustpilot.com/get_reviews

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/trustpilot.com/get_reviews
