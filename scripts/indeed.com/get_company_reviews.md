# Get Indeed company reviews

Automatically get Indeed company reviews on indeed.com. Get Indeed employee reviews for a company by its Indeed company slug (e.g. "Google", as it appears in indeed.com/cmp/<slug>), plus the overall rating and detailed-category ratings (work-life balance, pay and benefits, job security, management, culture). Anonymous, read-only.

- Site: indeed.com
- Address: `reduck/indeed.com/get_company_reviews`
- Updated: 2026-09-21 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/indeed.com/get_company_reviews`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/indeed.com/get_company_reviews
```

## Input

- `companySlug` (string, required): Indeed company slug from the /cmp/<slug> URL, e.g. "Google" — the slug only, not a full URL.
- `page` (integer, optional): Reviews page number. Indeed paginates with a client-side Next button, so the script steps forward page-1 times; a high number costs a step per page. Paging past the last page yields no review cards.

## Output

- `found` (boolean, required): Reports only that the slug did not return HTTP 404. Indeed is inconsistent here — measured: some unknown slugs 404 while others are served a page — so found:true is NOT proof the company exists. Treat a non-null `name` or `rating` as the real existence signal.
- `companySlug` (string, required)
- `url` (string | null, optional)
- `name` (string | null, optional): Company name as Indeed renders it; null when the page carried no company data. Together with `rating`, this is the reliable signal that the company is real.
- `page` (integer, optional)
- `rating` (number | null, optional)
- `reviews` (array, optional)
- `reviewCount` (integer | null, optional)
- `reviewsBlocked` (boolean, optional): True when the page carried no review cards and no aggregate-rating data. Usually Indeed's 'Additional Verification Required' anti-automation interstitial, but the same reading occurs when paging past the last page or when the slug does not name a real company, so it means 'no reviews were readable here', not specifically 'we were blocked'.
- `categoryRatings` (array, optional): Whatever detailed-category rating rows the page shows (e.g. work-life balance, pay and benefits) - the label text as Indeed renders it.

## FAQ

### What does "Get Indeed company reviews" do?

Get Indeed employee reviews for a company by its Indeed company slug (e.g. "Google", as it appears in indeed.com/cmp/<slug>), plus the overall rating and detailed-category ratings (work-life balance, pay and benefits, job security, management, culture). Anonymous, read-only.

### How do I automatically get Indeed company reviews on indeed.com?

Ask an AI agent connected to Reduck to run reduck/indeed.com/get_company_reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/indeed.com/get_company_reviews

### Is there a indeed.com API to get Indeed company reviews?

You do not need one. "Get Indeed company reviews" drives the real indeed.com pages in a browser, so it works whether or not indeed.com offers an API for this.

### What information do I need to provide?

Required: companySlug. Optional: page.

### What does it return?

It returns url, name, page, found, rating, reviews, companySlug, reviewCount, reviewsBlocked, categoryRatings.

### Do I need to be logged in to indeed.com?

No. It only uses pages of indeed.com that are reachable without signing in.

### Does it change anything on indeed.com, or only read data?

It only reads. It looks things up on indeed.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/indeed.com/get_company_reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/indeed.com/get_company_reviews

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/indeed.com/get_company_reviews
