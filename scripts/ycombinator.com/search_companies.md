# Search YC startup directory

Automatically search YC startup directory on ycombinator.com. Pull YC companies by batch, tag, region or hiring status with websites and team sizes.

- Site: ycombinator.com
- Address: `reduck/ycombinator.com/search_companies`
- Updated: 2026-10-05 (v2)
- Author: Reduck AI (reduck)

## About

Send the filters as JSON and get back plain rows for each matching company, with website, oneLiner, batch, teamSize, isHiring and tags. A free-text query is accepted too. Say you sell an API monitoring product to young developer tool startups. You ask for tag "Developer Tools", batches "Spring 2026" and "Summer 2026" and isHiring true, which should fit on one page at the default 40 rows. Sort by teamSize, keep the rows under 15 people, and open each company's url to find the founders before you write to anyone. The directory's company size filter is not exposed here, so size is something you trim after the fetch. Values inside one filter are OR'd, and separate filters are AND'd. The script reads the search key from the directory page on each run and queries the search index directly, so no YC account is needed.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ycombinator.com/search_companies`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ycombinator.com/search_companies
```

## Input

- `tag` (array, optional): Tags, e.g. ["Artificial Intelligence","SaaS","Developer Tools"]. OR within the list.
- `page` (integer, optional): Zero-based page index. Loop it up to nbPages-1 to fetch everything.
- `batch` (array, optional): Filter to these YC batches, e.g. ["Summer 2023","Winter 2024"]. OR within the list.
- `count` (integer, optional): Alias for hitsPerPage — results per page. Takes precedence over hitsPerPage when both are set.
- `query` (string, optional): Free-text search (company name, description, tags). Empty = browse the whole directory.
- `region` (array, optional): HQ regions, e.g. ["United States of America","Europe","Remote"]. OR within the list.
- `status` (array, optional): Company status. OR within the list.
- `industry` (array, optional): Top-level industry categories, e.g. ["Fintech","B2B","Healthcare"]. OR within the list.
- `isHiring` (boolean, optional): Only companies currently hiring (true filters; false/omitted = no filter).
- `nonprofit` (boolean, optional): Only nonprofits (true filters; false/omitted = no filter).
- `topCompany` (boolean, optional): Only YC top companies (true filters; false/omitted = no filter).
- `hitsPerPage` (integer, optional): Results per page (Algolia caps at 1000). Alias: count.

## Output

- `page` (integer, required)
- `total` (integer, required): Total matches across all pages.
- `nbPages` (integer, required)
- `companies` (array, required)
- `hitsPerPage` (integer, optional)

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "page": 1,
  "total": 3,
  "nbPages": 3,
  "companies": [
    {
      "id": "abc123",
      "url": "https://example.com/item/123",
      "name": "Example",
      "slug": "…",
      "tags": [
        "…"
      ],
      "batch": "…",
      "stage": "…",
      "status": "…",
      "logoUrl": "https://example.com/item/123",
      "regions": [
        "…"
      ],
      "website": "…",
      "industry": "…",
      "isHiring": true,
      "location": "…",
      "oneLiner": "…",
      "teamSize": 3,
      "nonprofit": true,
      "industries": [
        "…"
      ],
      "launchedAt": "2026-01-15T09:30:00Z",
      "topCompany": true,
      "subindustry": "…",
      "longDescription": "…"
    }
  ],
  "hitsPerPage": 3
}
```

## FAQ

### What does "Search YC startup directory" do?

Search the YC startup directory (ycombinator.com/companies) by free-text query plus filters such as batch, industry, tag, region, status, and top/hiring/nonprofit; each multi-value filter is OR'd within itself. Zero-based pagination.

### How do I automatically search YC startup directory on ycombinator.com?

Ask an AI agent connected to Reduck to run reduck/ycombinator.com/search_companies, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ycombinator.com/search_companies

### Is there a ycombinator.com API to search YC startup directory?

You do not need one. "Search YC startup directory" drives the real ycombinator.com pages in a browser, so it works whether or not ycombinator.com offers an API for this.

### What information do I need to provide?

Optional: tag, page, batch, count, query, region, status, industry, isHiring, nonprofit, topCompany, hitsPerPage.

### What does it return?

It returns page, total, nbPages, companies, hitsPerPage.

### Do I need to be logged in to ycombinator.com?

No. It only uses pages of ycombinator.com that are reachable without signing in.

### Does it change anything on ycombinator.com, or only read data?

Unknown: its author has not declared whether it changes anything on ycombinator.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ycombinator.com/search_companies, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ycombinator.com/search_companies

### Who maintains it?

It is part of Reduck's official curated catalogue.

### How do I export every company in the YC directory?

Run one search per batch with count set to 1000 and read total and nbPages in each response. The schema notes that the search index caps a page at 1000 results, so paging one unfiltered query through the whole directory is the wrong approach. Splitting by batch keeps each query small, and you can merge the rows afterwards using the id field.

### Why does my YC batch filter return zero companies?

Filter values are matched as exact text against the directory's labels, so "W24" finds nothing while "Winter 2024" works. A misspelled tag, industry or region behaves the same way and gives an empty companies list rather than an error.

### Can I filter YC companies by team size or number of employees?

There is no team size input. Every result carries teamSize as a number, which can be null, so fetch the batch or tag you want and filter the rows afterwards, for example keeping teamSize of 10 or less.

### Can I search for companies that are not hiring?

No. isHiring, topCompany and nonprofit only filter when set to true, and leaving them out means no constraint. To find companies that are not hiring, fetch without isHiring and drop the rows where isHiring is true.

Source: https://reduck.ai/explore/scripts/reduck/ycombinator.com/search_companies
