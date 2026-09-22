# Search LinkedIn jobs

Automatically search LinkedIn jobs on linkedin.com. Search LinkedIn job postings by keywords, with optional location, date-posted window, workplace-type filter, sort, and pagination (25/page). Returns total, page, resolvedLocation, and jobs (jobId, title, company, location, benefits, postedAgo, easyApply, url). Searches worldwide by default, unlike LinkedIn's own UI which silently restricts to the viewer's country. Experience, salary, and industry filters are not exposed, and postedAgo is null when LinkedIn shows a "Viewed" marker instead of a date.

- Site: linkedin.com
- Address: `reduck/linkedin.com/search_jobs`
- Updated: 2026-09-17 (v13)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/search_jobs
```

## Input

- `keywords` (string, required): Free-text job search query, same as the jobs search box (e.g. "data engineer").
- `page` (integer, optional): 1-based page, 25 jobs per page. Caller loops while (page-1)*25 < total. Job lists move as postings open and close, so fanning out across pages can skip or duplicate a posting near an edit.
- `sortBy` (string, optional): Sort order. Defaults to relevance, matching LinkedIn's own default. "date" is canonical; "date_posted" is accepted as an alias for it, because the sibling script linkedin.com/search_posts spells the same concept that way.
- `location` (string, optional): Free-text location (e.g. "Paris, France", "Germany"). LinkedIn resolves it server-side with its own geo matching, so "Paris, France" becomes "Paris, Île-de-France, France". Omit it to search worldwide: the script asks for worldwide scope deliberately, because LinkedIn's own default quietly narrows results to the viewer's country.
- `datePosted` (string, optional): Posted-date window. Omit for any time.
- `workplaceTypes` (array, optional): Workplace-type filter, several allowed (matches any of them). Omit for all.

## Output

- `jobs` (array, required)
- `page` (integer, required)
- `total` (integer, required): Total matching postings for this filter, read from the SSR blob. 0 with empty jobs[] = no matching jobs (first-class outcome, not an error).
- `resolvedLocation` (string | null, optional): The location label LinkedIn resolved the free-text `location` arg to (e.g. "Paris, Île-de-France, France"), read from the search box. "Worldwide" when no location was given. Returned so the caller can detect a mis-resolved location.

## FAQ

### What does "Search LinkedIn jobs" do?

Search LinkedIn job postings by keywords, with optional location, date-posted window, workplace-type filter, sort, and pagination (25/page). Returns total, page, resolvedLocation, and jobs (jobId, title, company, location, benefits, postedAgo, easyApply, url). Searches worldwide by default, unlike LinkedIn's own UI which silently restricts to the viewer's country. Experience, salary, and industry filters are not exposed, and postedAgo is null when LinkedIn shows a "Viewed" marker instead of a date.

### How do I automatically search LinkedIn jobs on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/search_jobs

### Is there a linkedin.com API to search LinkedIn jobs?

You do not need one. "Search LinkedIn jobs" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: keywords. Optional: page, sortBy, location, datePosted, workplaceTypes.

### What does it return?

It returns jobs, page, total, resolvedLocation.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/search_jobs
