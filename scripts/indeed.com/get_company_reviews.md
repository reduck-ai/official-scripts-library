# Get Indeed company reviews

Automatically get Indeed company reviews on indeed.com. Get one page (20) of Indeed employee reviews for a company by its Indeed company slug (e.g. "Google", as in indeed.com/cmp/<slug>), with the company name, overall rating, total review count and the detailed category ratings (work-life balance, compensation and benefits, job security and advancement, management, culture). Each review has its id, link, title, text, rating, job title, location, current-employee flag and date. Fails when Indeed has no page for the slug, when the page is past the last one, or when Indeed shows its verification page instead of the reviews. Anonymous, read-only.

- Site: indeed.com
- Address: `reduck/indeed.com/get_company_reviews`
- Updated: 2026-10-28 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/indeed.com/get_company_reviews`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/indeed.com/get_company_reviews
```

## Input

- `companySlug` (string, required): Indeed company slug from the /cmp/<slug> URL, e.g. "Google" — the slug only, not a full URL.
- `page` (integer, optional): Reviews page number, 20 reviews per page. A page past the last one fails.

## Output

- `page` (integer, required)
- `reviews` (array, required)
- `companySlug` (string, required)
- `url` (string | null, optional)
- `name` (string | null, optional): Company name as Indeed gives it.
- `rating` (number | null, optional): Overall company rating out of 5.
- `reviewCount` (integer | null, optional): Total number of reviews Indeed counts for the company.
- `categoryRatings` (array, optional): Detailed category ratings out of 5.

## FAQ

### What does "Get Indeed company reviews" do?

Get one page (20) of Indeed employee reviews for a company by its Indeed company slug (e.g. "Google", as in indeed.com/cmp/<slug>), with the company name, overall rating, total review count and the detailed category ratings (work-life balance, compensation and benefits, job security and advancement, management, culture). Each review has its id, link, title, text, rating, job title, location, current-employee flag and date. Fails when Indeed has no page for the slug, when the page is past the last one, or when Indeed shows its verification page instead of the reviews. Anonymous, read-only.

### How do I automatically get Indeed company reviews on indeed.com?

Ask an AI agent connected to Reduck to run reduck/indeed.com/get_company_reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/indeed.com/get_company_reviews

### Is there a indeed.com API to get Indeed company reviews?

You do not need one. "Get Indeed company reviews" drives the real indeed.com pages in a browser, so it works whether or not indeed.com offers an API for this.

### What information do I need to provide?

Required: companySlug. Optional: page.

### What does it return?

It returns url, name, page, rating, reviews, companySlug, reviewCount, categoryRatings.

### Do I need to be logged in to indeed.com?

No. It only uses pages of indeed.com that are reachable without signing in.

### Does it change anything on indeed.com, or only read data?

It only reads. It looks things up on indeed.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/indeed.com/get_company_reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/indeed.com/get_company_reviews

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/indeed.com/get_company_reviews
