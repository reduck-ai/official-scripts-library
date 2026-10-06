# Search Glassdoor jobs

Automatically search Glassdoor jobs on glassdoor.com. Page-one Glassdoor job cards for a keyword and city, with company, rating, salary text, post age

- Site: glassdoor.com
- Address: `reduck/glassdoor.com/search_jobs`
- Updated: 2026-10-05 (v6)
- Author: Reduck AI (reduck)

## About

Give it a keyword and an optional city and you get Glassdoor's headline job count plus the roughly 30 listings on its first results page. Each listing carries a title, company, the employer's rating out of 5, location, a truncated snippet, the salary text when the card shows one, and a relative post age such as 8T. A backend developer weighing a move to Lyon would pass query "backend developer" with location "Lyon", drop anything rated under 3.5, and open the few that remain. Only page one is supported, because Glassdoor loads more results through a button that broke the page when clicked. Labels and links follow the locale Glassdoor picks for your connection, so a run from France can return French text and glassdoor.fr links. A location Glassdoor cannot match, or one it does not apply to the results, makes the run throw instead of searching everywhere.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/glassdoor.com/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/glassdoor.com/search_jobs
```

## Input

- `query` (string, required): Free-text job search query, same as Glassdoor's own search box (e.g. "data engineer").
- `location` (string, optional): Free-text city (e.g. "Paris", "Los Angeles"). Omit to search without a location filter. Resolved via Glassdoor's own autocomplete; an unrecognized or non-filtering location throws rather than silently returning unrelated/broader results.

## Output

- `jobs` (array, required)
- `total` (integer | null, required): Matching job count reported by Glassdoor's results headline. null if the headline couldn't be parsed.

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "jobs": [
    {
      "url": "https://example.com/item/123",
      "jobId": "abc123",
      "title": "Example",
      "rating": 3.5,
      "salary": "…",
      "company": "…",
      "snippet": "…",
      "location": "…",
      "postedAgo": "…"
    }
  ],
  "total": 3
}
```

## FAQ

### What does "Search Glassdoor jobs" do?

Search Glassdoor job listings by keyword and optional free-text location (city). Returns total and jobs (jobId, title, url, company, rating, location, salary, snippet, postedAgo) for the first results page (~30 listings — Glassdoor's pagination is a JS "load more" action, not a URL param, and was observed to break the page outright on click, so only page 1 is supported here). Location is resolved via Glassdoor's own place-autocomplete, preferring the first city-level match, because the top overall suggestion can be a broader state or region record that Glassdoor then silently fails to filter by; an unrecognized or non-filtering location throws. Glassdoor serves the UI (and some listing labels like the skills line) in whatever language/locale it geo-resolves the session to, independent of the job's own country — text fields may not be in English or in the language of the job itself. Distinct from the existing search_companies/get_company scripts, which cover company profiles and reviews, not job postings.

### How do I automatically search Glassdoor jobs on glassdoor.com?

Ask an AI agent connected to Reduck to run reduck/glassdoor.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/glassdoor.com/search_jobs

### Is there a glassdoor.com API to search Glassdoor jobs?

You do not need one. "Search Glassdoor jobs" drives the real glassdoor.com pages in a browser, so it works whether or not glassdoor.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: location.

### What does it return?

It returns jobs, total.

### Do I need to be logged in to glassdoor.com?

No. It only uses pages of glassdoor.com that are reachable without signing in.

### Does it change anything on glassdoor.com, or only read data?

It only reads. It looks things up on glassdoor.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/glassdoor.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/glassdoor.com/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

### Can I get more than 30 Glassdoor job results per search?

A Glassdoor job search returns only the first results page, about 30 listings, even when the headline total is far larger. Glassdoor loads more through a load more button rather than a page number in the URL, and clicking it broke the page when observed. To cover more ground, run several narrower searches, such as keyword variants or nearby cities, and merge the results on jobId.

### Why do Glassdoor job results come back in French or German when I searched an English job title?

Glassdoor picks its interface language from where your connection appears to be, not from the job's country. Snippets, the skills line and the postedAgo label can come back localized, with values like 8T or 30T+, and listing links can point to a country domain such as glassdoor.fr instead of glassdoor.com.

### How do I get more detail on the companies in my Glassdoor job results?

Job results give the company name but no employer ID, so look the name up with search_companies and check the match by hand, since it returns fuzzy suggestions that can include near-names. The employerId from the right match goes into get_company for the overall rating and related company figures. Pay data is not per company: get_salaries works per job title and country.

Source: https://reduck.ai/explore/scripts/reduck/glassdoor.com/search_jobs
