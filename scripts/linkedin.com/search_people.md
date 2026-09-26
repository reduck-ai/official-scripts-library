# Search LinkedIn people

Automatically search LinkedIn people on linkedin.com. Search LinkedIn people by keywords with optional title, name, company, school, currentCompanyIds/pastCompanyIds (numeric ids from get_company_info), connectionDegrees, connectionOf, location, and pagination (10/page). Returns page, total, locationResolved, and people (name, url, publicId, memberUrn, degree, headline, location, snippet, followers, mutualConnections).

- Site: linkedin.com
- Address: `reduck/linkedin.com/search_people`
- Updated: 2026-09-25 (v17)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/search_people`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/search_people
```

## Input

- `page` (integer, optional): Result page, 10 people per page. Default 1. Pagination verified deterministic (same page from two fresh cold sessions returned identical people in identical order — safe to fan out). LinkedIn caps browsing at ~100 pages; free-tier accounts also hit a monthly commercial-use search limit.
- `title` (string, optional): Current job title keyword (LinkedIn 'Title' filter, exact-phrase quoted).
- `geoUrn` (string | array, optional): LinkedIn geo URN id(s) — the location facet, OR-combined (source from suggest_locations). Pure URL templating, no UI; takes precedence over `location`.
- `school` (string, optional): School name keyword.
- `company` (string, optional): Company name keyword (free-text 'Company' filter — use currentCompanyIds for an exact company).
- `keywords` (string, optional): Free-text search query.
- `lastName` (string, optional): Last name filter.
- `location` (string, optional): Free-text location ('Paris'). Resolved to LinkedIn's best-matching place; the applied label is returned as locationResolved — check it when the name is ambiguous (Paris, Texas...) or has no single LinkedIn geo (a continent like 'Europe'). Use suggest_locations + geoUrn for precision.
- `firstName` (string, optional): First name filter.
- `connectionOf` (string, optional): A member URN — the memberUrn value returned by this script's results or by get_profile (bare ACoAA… tail or full urn:li:fsd_profile:…, both accepted). Restricts results to that member's connections as LinkedIn reveals them to you: for a member outside your 1st degree that is exactly the people you have in common — your possible introducers. Works alone (no other filter needed) and composes with every other facet.
- `pastCompanyIds` (array, optional): Numeric LinkedIn companyIds — past employer facet, OR-combined.
- `connectionDegrees` (array, optional): Connection-degree facet, OR-combined.
- `currentCompanyIds` (array, optional): Numeric LinkedIn companyIds (from get_company_info) — current employer facet, OR-combined.

## Output

- `page` (integer, required)
- `people` (array, required)
- `total` (integer | null, optional): Total result count if displayed; null when LinkedIn hides it (observed on free-tier accounts).
- `locationResolved` (string | null, optional): The geo suggestion label actually applied when args.location was given (else null) — inspect it to confirm the resolved place.

## FAQ

### What does "Search LinkedIn people" do?

Search LinkedIn people by keywords with optional title, name, company, school, currentCompanyIds/pastCompanyIds (numeric ids from get_company_info), connectionDegrees, connectionOf, location, and pagination (10/page). Returns page, total, locationResolved, and people (name, url, publicId, memberUrn, degree, headline, location, snippet, followers, mutualConnections).

### How do I automatically search LinkedIn people on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/search_people, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/search_people

### Is there a linkedin.com API to search LinkedIn people?

You do not need one. "Search LinkedIn people" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Optional: page, title, geoUrn, school, company, keywords, lastName, location, firstName, connectionOf, pastCompanyIds, connectionDegrees, currentCompanyIds.

### What does it return?

It returns page, total, people, locationResolved.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/search_people, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/search_people

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/search_people
