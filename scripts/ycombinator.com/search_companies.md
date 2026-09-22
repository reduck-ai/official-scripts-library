# Search YC startup directory

Automatically search YC startup directory on ycombinator.com. Search the YC startup directory (ycombinator.com/companies) by free-text query plus filters such as batch, industry, tag, region, status, and top/hiring/nonprofit; each multi-value filter is OR'd within itself. Zero-based pagination.

- Site: ycombinator.com
- Address: `reduck/ycombinator.com/search_companies`
- Updated: 2026-07-17 (v2)
- Author: Reduck AI (reduck)

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

Source: https://reduck.ai/explore/scripts/reduck/ycombinator.com/search_companies
