# Search Station F jobs

Automatically search Station F jobs on jobs.stationf.co. Up to 20 campus openings a call, with company size, contract type, remote policy and any posted pay.

- Site: jobs.stationf.co
- Address: `reduck/jobs.stationf.co/search_jobs`
- Updated: 2026-10-05 (v6)
- Author: Reduck AI (reduck)

## About

Station F's job board runs on Welcome to the Jungle and pools openings from campus companies, 566 of them on 5 October 2026, from startups listing two employees up to L'Oréal Groupe. Two employers hold over a quarter of them: Walter Learning with 85 roles, most of the Marseille and Madrid ones, and L'Oréal Groupe with 67. A student after a data internship would send query "data", contractType "Internship" and city "Paris". That matched 57 jobs (three pages of 20), 13 of them at L'Oréal, so sorting on company.employees puts the small teams first, though some companies leave headcount blank. Pay needs a second look. Only about half the listings give salary.minimum, and the period can be wrong. Guideflow's "Bras droit CEO" internship at 1,200 to 1,600 euros appears twice, once as monthly and once as daily. Welcome to the Jungle's own API serves one company's jobs at a time, and its all-companies endpoint needs a dedicated partnership.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/jobs.stationf.co/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/jobs.stationf.co/search_jobs
```

## Input

- `city` (string, optional): Exact city facet label as shown on the site, e.g. "Paris"
- `page` (integer, optional): 1-based page number. Must be within the visible pagination window for the current query/filters (throws otherwise).
- `query` (string, optional): Free-text keyword, e.g. "developer", "product manager"
- `department` (string, optional): Exact department/profession facet label as shown on the site, e.g. "Tech", "Business", "Sales", "Operations"
- `contractType` (string, optional): Exact contract-type facet label as shown on the site (English), e.g. "Full-Time", "Internship", "Apprenticeship", "Fixed-Term"

## Output

- `jobs` (array, optional)
- `page` (integer, optional)
- `total` (integer, optional)
- `totalPages` (integer, optional)

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "jobs": [
    {
      "id": "abc123",
      "url": "https://example.com/item/123",
      "slug": "…",
      "title": "Example",
      "office": "…",
      "remote": "…",
      "salary": {
        "period": "…",
        "maximum": 3.5,
        "minimum": 3.5,
        "currency": "…",
        "yearlyMinimum": 3.5
      },
      "company": {
        "name": "Example",
        "slug": "…",
        "logoUrl": "https://example.com/item/123",
        "employees": 3
      },
      "offices": "…",
      "promoted": true,
      "reference": "…",
      "department": "…",
      "profession": "…",
      "publishedAt": "2026-01-15T09:30:00Z",
      "contractType": "…",
      "contractTypeLabel": "…"
    }
  ],
  "page": 1,
  "total": 3,
  "totalPages": 3
}
```

## FAQ

### What does "Search Station F jobs" do?

Search job listings on Station F's public careers board (jobs.stationf.co, an embeddable careers widget aggregating openings across Station F resident startups) by free-text keyword and optional filters: department/profession (site's own category label, e.g. "Tech", "Business", "Sales", "Operations", "Comm / Marketing"), city (e.g. "Paris"), and contractType (site's own English label, e.g. "Full-Time", "Internship", "Apprenticeship", "Fixed-Term"). Filter values must match the site's own labels exactly — an unrecognized value throws rather than silently searching unfiltered. Pagination is 1-based via page; requesting a page beyond what's available throws rather than silently returning page 1. Returns total, page, totalPages, and jobs (id, reference, slug, title, url, company {name, slug, employees, logoUrl}, department, profession, contractType + contractTypeLabel, remote, salary, office, offices, publishedAt, promoted). A query/filter combination with no matches returns an empty jobs list, not an error.

### How do I automatically search Station F jobs on jobs.stationf.co?

Ask an AI agent connected to Reduck to run reduck/jobs.stationf.co/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/jobs.stationf.co/search_jobs

### Is there a jobs.stationf.co API to search Station F jobs?

You do not need one. "Search Station F jobs" drives the real jobs.stationf.co pages in a browser, so it works whether or not jobs.stationf.co offers an API for this.

### What information do I need to provide?

Optional: city, page, query, department, contractType.

### What does it return?

It returns jobs, page, total, totalPages.

### Do I need to be logged in to jobs.stationf.co?

No. It only uses pages of jobs.stationf.co that are reachable without signing in.

### Does it change anything on jobs.stationf.co, or only read data?

It only reads. It looks things up on jobs.stationf.co and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/jobs.stationf.co/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/jobs.stationf.co/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

### How do I get all Station F jobs, past the first 20?

Loop page from 1 to totalPages, which was 29 pages of 20 on 5 October 2026. Each call reloads the board and clicks Next until it reaches your page, so page 29 means 28 page turns first and a full sweep adds up to about 400; narrowing with a filter or a keyword first cuts both numbers. A page past totalPages fails with an error that gives the real count.

### Why does filtering by department (Profession on the board) fail or miss jobs?

The department input is the board's Profession filter, and its labels are not a fixed list: on 5 October 2026 there were 52, in English and French, including Business (98 jobs) and Opérations (7), and only 251 of 566 listings had one. The value must match exactly, accents included, so "Operations" fails while "Opérations" works. A keyword in query does not depend on that field, so it also finds jobs whose company left it blank.

### Can I search only remote Station F jobs, or one company's jobs?

There is no remote filter, but every job carries remote (fulltime, partial, punctual, no or unknown), and 36 listings were fully remote on 5 October 2026. The board's Company filter is not exposed either, so put the company name in query and check company.name in the results, because short names match loosely: "Joko" also pulled in jobs from Jool.

### Which contract types can I filter Station F jobs by?

Seven English labels, spelled exactly as the board shows them: on 5 October 2026 those were Full-Time (350 jobs), Internship (178), Freelance (18), Apprenticeship (16), Temporary, Graduate program and Part-Time. The list follows whatever is live, so "Fixed-Term", which no listing used that day, fails with an error naming it.

Source: https://reduck.ai/explore/scripts/reduck/jobs.stationf.co/search_jobs
