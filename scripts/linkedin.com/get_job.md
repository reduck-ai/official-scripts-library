# Get LinkedIn job

Automatically get LinkedIn job on linkedin.com. Fetch a LinkedIn job posting by numeric ID. Returns id, url, status (live/expired), title, company, location, posted, applicants, workplaceType, employmentType, description, and companyInfo (name, url, industry, followers, employeeRange, membersOnLinkedIn, description).

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_job`
- Updated: 2026-09-17 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_job`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_job
```

## Input

- `id` (string, required): LinkedIn numeric job ID (the trailing digits of a /jobs/view/... URL).

## Output

- `id` (string, required)
- `url` (string, required): Final URL after any redirect.
- `source` (string, required): Which renderer produced this result. member = the signed-in /jobs/view/ page, which carries the full 'About the company' card (followers, employee range, members on LinkedIn) but no job-criteria list. guest = the signed-out page, which carries the job-criteria list instead and only the company's name, URL and industry.
- `status` (string, required)
- `authenticated` (boolean, required): Whether the run had a LinkedIn session. False means the guest surface produced this result, which is thinner in company detail and richer in job criteria.
- `title` (string, optional)
- `posted` (string, optional): Localized relative time (e.g. 'il y a 2 jours', '2 days ago', 'vor 3 Tagen').
- `company` (string, optional)
- `criteria` (array, optional): Job-criteria list (seniority level, employment type, job function, industries), with localized keys. Present on the guest surface only; the member surface no longer renders it, so expect an empty array when source=member.
- `location` (string, optional)
- `applicants` (string | null, optional): Applicant-volume line from the top card. Null when LinkedIn hides it.
- `companyInfo` (object | null, optional): The company card. Null if absent. On the guest surface only name, url and industry are available.
- `description` (string, optional)
- `workplaceType` (string | null, optional): On-site | Remote | Hybrid (localized). Null when absent.
- `employmentType` (string | null, optional): Full-time, Part-time, Contract, Internship... (localized). Null when absent.

## FAQ

### What does "Get LinkedIn job" do?

Fetch a LinkedIn job posting by numeric ID. Returns id, url, status (live/expired), title, company, location, posted, applicants, workplaceType, employmentType, description, and companyInfo (name, url, industry, followers, employeeRange, membersOnLinkedIn, description).

### How do I automatically get LinkedIn job on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_job, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_job

### Is there a linkedin.com API to get LinkedIn job?

You do not need one. "Get LinkedIn job" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: id.

### What does it return?

It returns id, url, title, posted, source, status, company, criteria, location, applicants, companyInfo, description, authenticated, workplaceType, employmentType.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_job, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_job

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_job
