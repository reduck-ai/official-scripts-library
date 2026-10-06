# Search HelloWork jobs

Automatically search HelloWork jobs on hellowork.com. Pull 30 French job offers per page with company, city, contract, salary and a numeric jobId.

- Site: hellowork.com
- Address: `reduck/hellowork.com/search_jobs`
- Updated: 2026-10-05 (v4)
- Author: Reduck AI (reduck)

## About

Give it what you would type into HelloWork's two search boxes, say "data engineer" and "Lyon", and you get the 30 cards from that results page back as rows, each with a numeric jobId you can key a spreadsheet on. A business developer at a Lyon agency that places freelance data engineers could pull every page each morning (77 offers meant three runs when we checked) and diff the jobIds against yesterday's sheet. Any new jobId is a company hiring now and worth a call. The code sends no sort option, so the order is whatever HelloWork serves by default, and a new offer can land on any page. Text comes back as HelloWork prints it, in French, so postedAgo reads "il y a 4 jours" and salary is a raw string you parse yourself. It stops at the search cards: no full description and no applying.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hellowork.com/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hellowork.com/search_jobs
```

## Input

- `query` (string, required): Free-text job search query, same as HelloWork's own search box (e.g. "data engineer").
- `page` (integer, optional): 1-based page, 30 offers per page (HelloWork's own ?p= param).
- `location` (string, optional): Free-text location (e.g. "Paris", "Lyon"). Omit to search all of France.

## Output

- `jobs` (array, required)
- `page` (integer, required)
- `total` (integer, required): Matching offer count reported by HelloWork's own results header. 0 with empty jobs[] = no matching offers (first-class outcome, not an error).

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "jobs": [
    {
      "url": "https://example.com/item/123",
      "jobId": "abc123",
      "title": "Example",
      "salary": "…",
      "company": "…",
      "contract": "…",
      "location": "…",
      "postedAgo": "…",
      "remoteTag": "…",
      "superRecruiter": true
    }
  ],
  "page": 1,
  "total": 3
}
```

## FAQ

### What does "Search HelloWork jobs" do?

Search HelloWork's French job listings by keyword, optional free-text location, and page (30 offers/page). Returns total and jobs (jobId, title, company, url, location, contract, remoteTag, salary, superRecruiter, postedAgo). Salary and remote-work tags are only present when the listing/employer chose to show them, so they're frequently null.

### How do I automatically search HelloWork jobs on hellowork.com?

Ask an AI agent connected to Reduck to run reduck/hellowork.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hellowork.com/search_jobs

### Is there a hellowork.com API to search HelloWork jobs?

You do not need one. "Search HelloWork jobs" drives the real hellowork.com pages in a browser, so it works whether or not hellowork.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, location.

### What does it return?

It returns jobs, page, total.

### Do I need to be logged in to hellowork.com?

No. It only uses pages of hellowork.com that are reachable without signing in.

### Does it change anything on hellowork.com, or only read data?

It only reads. It looks things up on hellowork.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hellowork.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hellowork.com/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

### How many HelloWork offers can I get in one run?

One results page of 30 offers. The total field carries the count from HelloWork's own header, so divide it by 30, round up, and loop over page. Asking for a page past the last one returns an error instead of an empty list.

### Can I filter HelloWork results by contract type, télétravail or date posted?

No. Only query, location and page are sent, so HelloWork's sidebar filters stay at their defaults. To get CDI offers from the last day, fetch every page and keep rows where contract is "CDI" and postedAgo mentions "heures" rather than "jours".

### Are HelloWork results sorted by newest first?

Nothing in the inputs sets a sort order, so you get HelloWork's default ordering, which is not guaranteed to be by date. To catch fresh offers, fetch every page and compare jobId values with your previous run, or keep rows whose postedAgo is counted in hours.

### Why does remoteTag say "2 ans" instead of a télétravail status?

The field holds the third badge on the card, and on Alternance or Stage offers that badge can be the contract length, such as "2 ans". Read remoteTag next to contract. It is null when the card shows no third badge.

Source: https://reduck.ai/explore/scripts/reduck/hellowork.com/search_jobs
