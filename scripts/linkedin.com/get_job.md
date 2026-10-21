# Get LinkedIn job

Automatically get LinkedIn job on linkedin.com. Fetch one LinkedIn job posting by numeric id: pass the jobId of linkedin.com/search_jobs or get_company_jobs as jobId (or as id). Returns its title, LinkedIn's state of the posting (whether it still takes applications), creation date, whether it is reposted, its place and geo id, the labels and line under the title, the full description, the apply link or Easy Apply, whether you applied, and the company with its id, name, page, industry and industry id, member count, declared size and description. A posting LinkedIn does not have fails with a clear message, as does a browser that is not signed in.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_job`
- Updated: 2026-10-20 (v10)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_job`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_job
```

## Input

- `id` (string, optional): LinkedIn numeric job id: the jobId of linkedin.com/search_jobs, or the digits of a /jobs/view/ URL.
- `jobId` (string, optional): Same as id, under the name linkedin.com/search_jobs and get_company_jobs return it. Pass one of id or jobId.

## Output

- `id` (string, required)
- `url` (string, required): https://www.linkedin.com/jobs/view/<id>/
- `state` (string, required): LinkedIn's state of the posting: LISTED while it takes applications; another value (for example CLOSED) once it does not.
- `title` (string, required)
- `description` (string, required): The full job description text.
- `geoId` (string | null, optional): Geo id of that place, the form linkedin.com/search_jobs takes.
- `applied` (boolean, optional): Whether the signed-in member applied.
- `company` (object | null, optional): The company that posted the job. null when the posting names no company page.
- `applyUrl` (string | null, optional): The company's own application page, when the posting sends applicants there. null for Easy Apply.
- `location` (string | null, optional): The posting's place, for example "Denver, Colorado, United States".
- `reposted` (boolean, optional)
- `subtitle` (string | null, optional): The line under the title as LinkedIn shows it: place, when it was posted, applicant activity.
- `appliedAt` (string | null, optional)
- `createdAt` (string | null, optional): When the posting was created (ISO 8601). A reposted job keeps its first date here.
- `easyApply` (boolean, optional)
- `highlights` (array, optional): The labels under the title as LinkedIn shows them, for example the workplace type and the job type. In the account's interface language.

## FAQ

### What does "Get LinkedIn job" do?

Fetch one LinkedIn job posting by numeric id: pass the jobId of linkedin.com/search_jobs or get_company_jobs as jobId (or as id). Returns its title, LinkedIn's state of the posting (whether it still takes applications), creation date, whether it is reposted, its place and geo id, the labels and line under the title, the full description, the apply link or Easy Apply, whether you applied, and the company with its id, name, page, industry and industry id, member count, declared size and description. A posting LinkedIn does not have fails with a clear message, as does a browser that is not signed in.

### How do I automatically get LinkedIn job on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_job, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_job

### Is there a linkedin.com API to get LinkedIn job?

You do not need one. "Get LinkedIn job" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Optional: id, jobId.

### What does it return?

It returns id, url, geoId, state, title, applied, company, applyUrl, location, reposted, subtitle, appliedAt, createdAt, easyApply, highlights, description.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_job, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_job

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_job
