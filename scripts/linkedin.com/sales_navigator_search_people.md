# Sales Navigator: search people

Automatically search people on linkedin.com. Search LinkedIn Sales Navigator leads with the advanced filters (title, geography, seniority, function, company headcount, tenure, relationship, keywords, and more), paginated 25 per page via a 0-based start offset. At least one filter or keyword is required — start on its own is pagination, not a search. Returns total, count, start, and leads (leadId, fullName, memberUrn, degree, geoRegion, current title/company/industry, tenure, summary, spotlights, salesLeadUrl). Requires a Sales Navigator seat.

- Site: linkedin.com
- Address: `reduck/linkedin.com/sales_navigator_search_people`
- Updated: 2026-09-03 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/sales_navigator_search_people`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_search_people
```

## Input

- `start` (integer, optional): 0-based result offset; the page returns 25. Pass 0, 25, 50, ... to paginate. Order is stable across calls.
- `title` (string, optional): Current job title, free text (e.g. "CTO", "Head of Sales").
- `school` (string, optional): School, by name; resolved via the typeahead (first match wins). Prefer schoolId if you know it — skips the lookup and works regardless of the account's display language.
- `company` (string, optional): Current company, by name; resolved to a company id via the typeahead (first match wins, e.g. "Datadog"). Prefer companyId if you know it — skips the lookup and works regardless of the account's display language.
- `function` (array, optional): Job functions (OR).
- `industry` (string, optional): Industry, by name; resolved via the typeahead (first match wins). Prefer industryId if you know it — skips the lookup and works regardless of the account's display language (a caller-supplied English name may not match on a non-English LinkedIn account).
- `keywords` (string, optional): Free-text keyword box (matches across the profile).
- `lastName` (string, optional)
- `regionId` (integer, optional): Location ID, if you already know it — skips the location lookup entirely and works regardless of the account's display language.
- `schoolId` (integer, optional): School ID, if you already know it — skips the school lookup entirely. e.g. 14034 = Ecole Polytechnique.
- `companyId` (integer, optional): Company ID, if you already know it — skips the company lookup entirely.
- `firstName` (string, optional)
- `geography` (string, optional): Location, free text resolved server-side (e.g. "France", "Paris", "United States"). Prefer regionId if you know it — skips the lookup and works regardless of the account's display language.
- `pastTitle` (string, optional): Past job title, free text.
- `seniority` (array, optional): Seniority levels (OR).
- `industryId` (integer, optional): Industry ID, if you already know it — skips the industry lookup entirely.
- `changedJobs` (boolean, optional): Only leads who recently changed jobs (Recent updates toggle).
- `companyType` (array, optional): Current company type (OR).
- `pastCompany` (string, optional): Past company, by name; resolved via the typeahead (first match wins). Prefer pastCompanyId if you know it — skips the lookup and works regardless of the account's display language.
- `relationship` (array, optional): Connection degree (OR).
- `pastCompanyId` (integer, optional): Past company ID, if you already know it — skips the lookup entirely.
- `yearsAtCompany` (array, optional): Years at current company (OR).
- `yearsInPosition` (array, optional): Years in current position (OR).
- `companyHeadcount` (array, optional): Company headcount buckets (OR).
- `postedOnLinkedin` (boolean, optional): Only leads who recently posted on LinkedIn (Recent updates toggle).
- `yearsOfExperience` (array, optional): Total years of experience (OR).

## Output

- `count` (integer, required): Number of leads in this page (<=25).
- `leads` (array, required)
- `start` (integer, required)
- `total` (integer, required): Exact total matching leads (paging.total).
- `totalDisplay` (string | null, optional): LinkedIn's rounded display count (e.g. "180K+").

## FAQ

### What does "Sales Navigator: search people" do?

Search LinkedIn Sales Navigator leads with the advanced filters (title, geography, seniority, function, company headcount, tenure, relationship, keywords, and more), paginated 25 per page via a 0-based start offset. At least one filter or keyword is required — start on its own is pagination, not a search. Returns total, count, start, and leads (leadId, fullName, memberUrn, degree, geoRegion, current title/company/industry, tenure, summary, spotlights, salesLeadUrl). Requires a Sales Navigator seat.

### How do I automatically search people on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/sales_navigator_search_people, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_search_people

### Is there a linkedin.com API to search people?

You do not need one. "Sales Navigator: search people" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Optional: start, title, school, company, function, industry, keywords, lastName, regionId, schoolId, companyId, firstName, geography, pastTitle, seniority, industryId, changedJobs, companyType, pastCompany, relationship, pastCompanyId, yearsAtCompany, yearsInPosition, companyHeadcount, postedOnLinkedin, yearsOfExperience.

### What does it return?

It returns count, leads, start, total, totalDisplay.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

Unknown: its author has not declared whether it changes anything on linkedin.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/sales_navigator_search_people, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_search_people

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/sales_navigator_search_people
