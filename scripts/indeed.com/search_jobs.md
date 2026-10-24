# Search Indeed jobs

Automatically search Indeed jobs on indeed.com. First page of Indeed job cards with salary text, posting age and a jobKey to diff between runs

- Site: indeed.com
- Address: `reduck/indeed.com/search_jobs`
- Updated: 2026-10-22 (v9)
- Author: Reduck AI (reduck)

## About

Say you're hunting for a data analyst job in Austin. Run query "data analyst", location "Austin, TX" and sortBy "date" each morning, compare the jobKey values with yesterday's list, and open only new ones with a salary. Each run returns one results page of job cards, with salary as raw text when Indeed shows one and postedAgo as a phrase like "3 days ago". Outside the US, set country to "fr", "de" or "uk" so the location belongs to that country's Indeed site. If outOfCountry comes back true, Indeed swapped your location for generic results and total means nothing. Two limits apply. Anonymous search only works for page 1, so narrow the query instead of paging. And Indeed can bounce datacenter traffic to a login page, so a hosted run needs an in-country residential proxy, while your own Chrome sends the search from your home connection. You get the viewjob link, not the job description.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/indeed.com/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/indeed.com/search_jobs
```

## Input

- `query` (string, required): Free-text job search query, same as Indeed's search box (e.g. "data engineer"). Must be non-empty — an empty query redirects Indeed to its homepage instead of a results page.
- `page` (integer, optional): 1-based page. Only page=1 is reliably supported anonymously — Indeed shows a sign-in wall for further pages, which the script surfaces as a thrown error.
- `radius` (integer, optional): Distance around `location`, from Indeed's distance menu: miles on www.indeed.com, kilometres on most other country sites; 0 = exact location only. Omit for Indeed's default (25).
- `sortBy` (string, optional): Sort order. Default: relevance (Indeed's own default).
- `country` (string, optional): Indeed country site to search, as its subdomain code (e.g. "us", "fr", "de", "uk", "ca"). Lowercased; "us" maps to www.indeed.com, others to "<country>.indeed.com".
- `location` (string, optional): Free-text location (e.g. "Paris", "Berlin"). Must match the chosen country site or Indeed marks the result outOfCountry and returns unrelated jobs.
- `jobTypeId` (string, optional): Indeed's id for one job type, as its own job-type filter puts it in the URL (`sc=0kf:attr(<id>);`), e.g. "CF3CP" = full-time. Omit for every job type.
- `postedWithinDays` (integer, optional): Only jobs posted in the last 1, 3, 7 or 14 days (Indeed's date-posted menu). Omit for any date.

## Output

- `jobs` (array, required)
- `page` (integer, required)
- `total` (integer, required): Matching job count reported by Indeed for this query/location.
- `outOfCountry` (boolean | null, required): Indeed's own flag, as it sends it: true when Indeed treats this browser as visiting the country site from outside that country. Indeed judges it from the browser's network, not from the location searched. null when this run could not read it (e.g. a search with no jobs, where Indeed sends no job-card data).

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "jobs": [
    {
      "url": "https://example.com/item/123",
      "title": "Example",
      "jobKey": "…",
      "remote": true,
      "salary": "…",
      "company": "…",
      "jobTypes": [
        "…"
      ],
      "location": "…",
      "postedAgo": "…",
      "sponsored": true
    }
  ],
  "page": 1,
  "total": 3,
  "outOfCountry": true
}
```

## FAQ

### What does "Search Indeed jobs" do?

Search Indeed's public job listings by keyword, optional free-text location and country site (e.g. "fr" for fr.indeed.com, default "us"). Filters: distance around the location, posted within 1/3/7/14 days, and one job type by Indeed's id (e.g. "CF3CP" = full-time, the code Indeed's own job-type filter puts in its URL). Returns total, page, outOfCountry (whether Indeed treats this browser as visiting from outside that country; null when it could not be read, as on a search with no jobs), and jobs (jobKey, title, company, location, salary, jobTypes, remote, sponsored, postedAgo, url). No match returns total 0 and an empty jobs list. Only page 1 is available without signing in; a later page, or a search Indeed refuses to serve, fails with a message that says so.

### How do I automatically search Indeed jobs on indeed.com?

Ask an AI agent connected to Reduck to run reduck/indeed.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/indeed.com/search_jobs

### Is there a indeed.com API to search Indeed jobs?

You do not need one. "Search Indeed jobs" drives the real indeed.com pages in a browser, so it works whether or not indeed.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, radius, sortBy, country, location, jobTypeId, postedWithinDays.

### What does it return?

It returns jobs, page, total, outOfCountry.

### Do I need to be logged in to indeed.com?

No. It only uses pages of indeed.com that are reachable without signing in.

### Does it change anything on indeed.com, or only read data?

Unknown: its author has not declared whether it changes anything on indeed.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/indeed.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/indeed.com/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

### Can I get more than the first page of Indeed results?

Not anonymously. The script is built for page 1. Indeed answers page 2 and beyond in an anonymous session with a sign-in wall, and the script reports that as a pagination error instead of returning an empty list. Whether a signed-in session would work is untested. To see different postings, narrow the query or location, or sort by date so the newest jobs land on page 1.

### Why does a search for jobs in Paris, France on indeed.com return unrelated jobs?

Each Indeed country site searches its own market. A location outside the US on www.indeed.com is treated as out of country, so outOfCountry is true and the page holds fallback listings. Pass country "fr" to search fr.indeed.com instead, and ignore total whenever outOfCountry is true.

### Why did my Indeed search stop with a sign-in wall error on page 1?

Indeed sometimes redirects requests from datacenter IP addresses to its login page, and the script stops with an error that names the network as the cause. Retry from a residential connection. On a Reduck-hosted browser, pass a country such as FR so the session goes through an in-country residential proxy. Your own Chrome is another route, with mixed results so far.

Source: https://reduck.ai/explore/scripts/reduck/indeed.com/search_jobs
