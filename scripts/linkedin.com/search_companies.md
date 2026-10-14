# Search LinkedIn companies

Automatically search LinkedIn companies on linkedin.com. Search LinkedIn companies by keywords, with an optional company-size filter and a page number (10 companies per page). Returns page, total, hasNextPage and companies (name, url, slug, companyId, pageType, industry, location, snippet, followers, and pageBy, the parent company page of a showcase page). companyId is the id that linkedin.com/search_people takes as currentCompanyIds. The results also include showcase and school pages.

- Site: linkedin.com
- Address: `reduck/linkedin.com/search_companies`
- Updated: 2026-10-13 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/search_companies`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/search_companies
```

## Input

- `keywords` (string, required): Free-text search query.
- `page` (integer, optional): Result page, 10 companies per page. Default 1. Pagination verified deterministic: fetching the same page twice from fresh cold sessions returns identical order (incl. snippets), and consecutive pages do not overlap — safe to fan out pages in parallel. LinkedIn caps browsing at ~100 pages (~1000 companies) regardless of the displayed total.
- `companySizes` (array, optional): Employee-count buckets, OR-combined — pass each bucket as its own array element (do not comma-join multiple buckets into one string element). Human values: 1-10, 11-50, 51-200, 201-500, 501-1000, 1001-5000, 5001-10000, 10001+ (surrounding whitespace/commas on a single element are tolerated) or LinkedIn codes B,C,D,E,F,G,H,I in that order.

## Output

- `page` (integer, required)
- `total` (integer | null, required): The result count LinkedIn shows above the list. 0 on its empty state. Null when the page shows no count. Paging stops at about 100 pages (about 1000 companies) however large this number is.
- `companies` (array, required): The companies on this page, in LinkedIn order. Empty only when LinkedIn shows its empty state.
- `hasNextPage` (boolean | null, required): Whether LinkedIn offers a next page. False on the last page and on the empty state. Null only when a full page shows no pager.

## FAQ

### What does "Search LinkedIn companies" do?

Search LinkedIn companies by keywords, with an optional company-size filter and a page number (10 companies per page). Returns page, total, hasNextPage and companies (name, url, slug, companyId, pageType, industry, location, snippet, followers, and pageBy, the parent company page of a showcase page). companyId is the id that linkedin.com/search_people takes as currentCompanyIds. The results also include showcase and school pages.

### How do I automatically search LinkedIn companies on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/search_companies, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/search_companies

### Is there a linkedin.com API to search LinkedIn companies?

You do not need one. "Search LinkedIn companies" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: keywords. Optional: page, companySizes.

### What does it return?

It returns page, total, companies, hasNextPage.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/search_companies, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/search_companies

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/search_companies
