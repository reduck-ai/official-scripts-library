# Search LinkedIn jobs

Automatically search LinkedIn jobs on linkedin.com. Search LinkedIn job postings by keywords, with every filter LinkedIn's jobs search offers: place (geoId from linkedin.com/suggest_locations, or free text), date posted, experience level, job type, workplace type, distance, salary, company, industry, job function, title, benefits, commitments, places inside the area, Easy Apply, under 10 applicants, verified, in your network and fair chance employer. Filters that take ids get them from linkedin.com/list_job_filters. Returns 25 jobs per page in LinkedIn's order, the total, and the place LinkedIn searched in (geoId and name), with each job's id, title, company and company id, location, the line under it (salary or benefits), when it was listed, and whether it is reposted, promoted or Easy Apply. Searches worldwide when no place is given, unlike LinkedIn's interface, which narrows to the viewer's country. A search with no match returns total 0 and an empty list. Fails with a clear message when the browser is not signed in or LinkedIn limits the account.

- Site: linkedin.com
- Address: `reduck/linkedin.com/search_jobs`
- Updated: 2026-10-19 (v17)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/search_jobs
```

## Input

- `keywords` (string, required): Free-text job search query, the same as the jobs search box (for example "data engineer").
- `page` (integer, optional): 1-based page, 25 jobs per page. Read the next page while (page - 1) * 25 < total. Postings open and close between calls, so a posting near a page edge can be skipped or repeated.
- `geoId` (string, optional): LinkedIn geo id of the place to search in. Get it from linkedin.com/suggest_locations (its geoUrn). Takes precedence over location. Omit both to search worldwide.
- `sortBy` (string, optional): Sort order. "date" is newest first; "date_posted" means the same, the spelling linkedin.com/search_posts uses.
- `jobTypes` (array, optional): Job types. A job matches any of them. Omit for all.
- `location` (string, optional): Free-text place (for example "Paris, France"). LinkedIn picks the place itself; the result returns the geoId and name it picked. Prefer geoId when you need one exact place.
- `placeIds` (array, optional): Places inside the searched area (for example a city of a metro area), as geo ids from the location filter of linkedin.com/list_job_filters.
- `titleIds` (array, optional): Job title ids, from linkedin.com/list_job_filters. A job matches any of them.
- `easyApply` (boolean, optional): Only jobs with Easy Apply.
- `benefitIds` (array, optional): Benefit ids, from linkedin.com/list_job_filters. A job matches any of them.
- `companyIds` (array, optional): Numeric LinkedIn company ids, from linkedin.com/get_company_info, linkedin.com/search_companies, linkedin.com/list_job_filters, or the companyId of a job in this result. A job matches any of them.
- `datePosted` (string, optional): Posted-date window. Omit for any time.
- `industryIds` (array, optional): Industry ids, from linkedin.com/list_job_filters. A job matches any of them.
- `salaryBucket` (integer, optional): Minimum salary, as LinkedIn's bucket number. In the United States: 1 is $40,000+, 2 is $60,000+, and so on in steps of $20,000 up to 9, $200,000+. LinkedIn offers this filter only in some countries; linkedin.com/list_job_filters shows the buckets of a search.
- `verifiedOnly` (boolean, optional): Only jobs with verifications.
- `commitmentIds` (array, optional): Company commitment ids, from linkedin.com/list_job_filters. A job matches any of them.
- `distanceMiles` (integer, optional): Radius around the place, in miles. 0 is the exact place. Omit for LinkedIn's default (25 miles in its interface).
- `functionCodes` (array, optional): Job function codes (for example "eng"), from linkedin.com/list_job_filters. A job matches any of them.
- `inYourNetwork` (boolean, optional): Only jobs at companies where you have connections.
- `workplaceTypes` (array, optional): Workplace types. A job matches any of them. Omit for all.
- `experienceLevels` (array, optional): Experience levels. A job matches any of them. Omit for all.
- `under10Applicants` (boolean, optional): Only jobs with fewer than 10 applicants.
- `fairChanceEmployer` (boolean, optional): Only jobs from fair chance employers.

## Output

- `jobs` (array, required)
- `page` (integer, required)
- `total` (integer, required): Number of postings that match, as LinkedIn counts them for this search. 0 with an empty jobs list means no posting matches.
- `geoId` (string | null, optional): Geo id of the place LinkedIn searched in. 92000000 is worldwide.
- `resolvedLocation` (string | null, optional): Name of that place, so you can check LinkedIn picked the place you meant.

## FAQ

### What does "Search LinkedIn jobs" do?

Search LinkedIn job postings by keywords, with every filter LinkedIn's jobs search offers: place (geoId from linkedin.com/suggest_locations, or free text), date posted, experience level, job type, workplace type, distance, salary, company, industry, job function, title, benefits, commitments, places inside the area, Easy Apply, under 10 applicants, verified, in your network and fair chance employer. Filters that take ids get them from linkedin.com/list_job_filters. Returns 25 jobs per page in LinkedIn's order, the total, and the place LinkedIn searched in (geoId and name), with each job's id, title, company and company id, location, the line under it (salary or benefits), when it was listed, and whether it is reposted, promoted or Easy Apply. Searches worldwide when no place is given, unlike LinkedIn's interface, which narrows to the viewer's country. A search with no match returns total 0 and an empty list. Fails with a clear message when the browser is not signed in or LinkedIn limits the account.

### How do I automatically search LinkedIn jobs on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/search_jobs

### Is there a linkedin.com API to search LinkedIn jobs?

You do not need one. "Search LinkedIn jobs" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: keywords. Optional: page, geoId, sortBy, jobTypes, location, placeIds, titleIds, easyApply, benefitIds, companyIds, datePosted, industryIds, salaryBucket, verifiedOnly, commitmentIds, distanceMiles, functionCodes, inYourNetwork, workplaceTypes, experienceLevels, under10Applicants, fairChanceEmployer.

### What does it return?

It returns jobs, page, geoId, total, resolvedLocation.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/search_jobs
