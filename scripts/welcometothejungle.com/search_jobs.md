# Search Welcome to the Jungle jobs

Automatically search Welcome to the Jungle jobs on welcometothejungle.com. Search job offers on Welcome to the Jungle by keyword, with optional filters for language edition, office country, contract type and remote policy. Returns one page of offers with title, link, company, contract type, remote policy, cities, salary range where published, publication date and summary, plus the total count and number of pages. At most the first 1,000 offers of a search can be paged through, so narrow broad searches with filters. No sign-in needed.

- Site: welcometothejungle.com
- Address: `reduck/welcometothejungle.com/search_jobs`
- Updated: 2026-09-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/welcometothejungle.com/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/welcometothejungle.com/search_jobs
```

## Input

- `page` (integer, optional): Zero-based results page.
- `query` (string, optional): Free text: a job title, skill or company. Empty lists every offer.
- `remote` (string, optional): Remote policy filter.
- `language` (string, optional): Which language edition of Welcome to the Jungle to search.
- `countryCode` (string, optional): Two-letter office country code to filter on, e.g. FR, ES, CZ.
- `hitsPerPage` (integer, optional)
- `contractType` (string, optional): Contract type as Welcome to the Jungle stores it, e.g. full_time, internship, apprenticeship, temporary, freelance.

## Output

- `jobs` (array, required)
- `page` (number, required)
- `query` (string, required)
- `total` (number, required)
- `totalPages` (number, required)

## FAQ

### What does "Search Welcome to the Jungle jobs" do?

Search job offers on Welcome to the Jungle by keyword, with optional filters for language edition, office country, contract type and remote policy. Returns one page of offers with title, link, company, contract type, remote policy, cities, salary range where published, publication date and summary, plus the total count and number of pages. At most the first 1,000 offers of a search can be paged through, so narrow broad searches with filters. No sign-in needed.

### How do I automatically search Welcome to the Jungle jobs on welcometothejungle.com?

Ask an AI agent connected to Reduck to run reduck/welcometothejungle.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcometothejungle.com/search_jobs

### Is there a welcometothejungle.com API to search Welcome to the Jungle jobs?

You do not need one. "Search Welcome to the Jungle jobs" drives the real welcometothejungle.com pages in a browser, so it works whether or not welcometothejungle.com offers an API for this.

### What information do I need to provide?

Optional: page, query, remote, language, countryCode, hitsPerPage, contractType.

### What does it return?

It returns jobs, page, query, total, totalPages.

### Do I need to be logged in to welcometothejungle.com?

No. It only uses pages of welcometothejungle.com that are reachable without signing in.

### Does it change anything on welcometothejungle.com, or only read data?

It only reads. It looks things up on welcometothejungle.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/welcometothejungle.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcometothejungle.com/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/welcometothejungle.com/search_jobs
