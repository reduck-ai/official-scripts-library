# Get LinkedIn company jobs

Automatically get LinkedIn company jobs on linkedin.com. Get a LinkedIn company's open job postings by numeric company id (from linkedin.com/get_company_info or search_companies), worldwide unless a geoId is given, with an optional keyword filter, 25 per page. Returns the total, the company name LinkedIn filtered on, and the jobs in the same shape as linkedin.com/search_jobs (id, title, location, the line under it, when it was listed, reposted, promoted, Easy Apply). companyName is null when LinkedIn does not list the company in its filter, which is what an id it does not know gives; a known company with no openings returns total 0. For other filters, use search_jobs with companyIds. Fails with a clear message when the browser is not signed in or LinkedIn limits the account.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_company_jobs`
- Updated: 2026-10-29 (v10)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_company_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_company_jobs
```

## Input

- `companyId` (string | integer, required): Numeric LinkedIn company id (for example 1035), from linkedin.com/get_company_info or linkedin.com/search_companies. Slugs are not accepted.
- `page` (integer, optional): 1-based page, 25 jobs per page. Read the next page while (page - 1) * 25 < total. Postings open and close between calls, so a posting near a page edge can be skipped or repeated.
- `geoId` (string | integer, optional): LinkedIn geo id to limit the openings to a place, from linkedin.com/suggest_locations. Omit for worldwide: LinkedIn's own interface otherwise narrows the list to the viewer's country.
- `keywords` (string, optional): Free-text filter within the company's openings, the same as the search box.

## Output

- `jobs` (array, required)
- `page` (integer, required)
- `total` (integer, required): Number of open postings that match, as LinkedIn counts them. 0 with an empty jobs list means the company has no matching openings.
- `companyId` (string, required)
- `companyName` (string | null, optional): The company LinkedIn filtered on, as its filter shows it. null when LinkedIn did not list the company in its filter.

## FAQ

### What does "Get LinkedIn company jobs" do?

Get a LinkedIn company's open job postings by numeric company id (from linkedin.com/get_company_info or search_companies), worldwide unless a geoId is given, with an optional keyword filter, 25 per page. Returns the total, the company name LinkedIn filtered on, and the jobs in the same shape as linkedin.com/search_jobs (id, title, location, the line under it, when it was listed, reposted, promoted, Easy Apply). companyName is null when LinkedIn does not list the company in its filter, which is what an id it does not know gives; a known company with no openings returns total 0. For other filters, use search_jobs with companyIds. Fails with a clear message when the browser is not signed in or LinkedIn limits the account.

### How do I automatically get LinkedIn company jobs on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_company_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_company_jobs

### Is there a linkedin.com API to get LinkedIn company jobs?

You do not need one. "Get LinkedIn company jobs" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: companyId. Optional: page, geoId, keywords.

### What does it return?

It returns jobs, page, total, companyId, companyName.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_company_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_company_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_company_jobs
