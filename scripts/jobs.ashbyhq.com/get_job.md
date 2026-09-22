# Get Ashby job posting

Automatically get Ashby job posting on jobs.ashbyhq.com. Read one Ashby job posting (jobs.ashbyhq.com/&lt;board&gt;/&lt;jobId&gt;), description HTML included.

- Site: jobs.ashbyhq.com
- Address: `reduck/jobs.ashbyhq.com/get_job`
- Updated: 2026-08-03 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/jobs.ashbyhq.com/get_job`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/jobs.ashbyhq.com/get_job
```

## Input

- `board` (string, required): Board slug in the URL jobs.ashbyhq.com/<board>, e.g. "lassie" or "ramp". Case-sensitive; a posting is only reachable under its own board.
- `jobId` (string, required): Posting id, as returned by list_jobs.

## Output

- `id` (string, required): Posting id as the page reports it — compare with the requested jobId.
- `title` (string, required)
- `teamNames` (array, required): Department chain, root first, leaf last. Boards that show sub-teams render the whole chain on the Department line; the others render just the root.
- `descriptionHtml` (string, required): Full job description as the HTML the page renders, verbatim.
- `department` (string | null, optional): Top-level department — the root of teamNames, and the same value list_jobs returns.
- `locationName` (string | null, optional): Primary location.
- `workplaceType` (string | null, optional): Ashby's raw value — "OnSite", "Hybrid", "Remote" (the page's Location Type spells these "On-site" etc.). Null when the posting does not state one, and then the page shows no Location Type.
- `employmentType` (string | null, optional): Ashby's raw value — "FullTime", "PartTime", "Contract", "Intern" (the page spells these "Full time" etc.).
- `compensationTiers` (array, optional): Pay bands as the Compensation section lists them; empty when the posting shows no pay. A posting with one unnamed band has a single entry whose title is null.
- `applicationDeadline` (string | null, optional): ISO instant; the page renders it as a local date and time ("Deadline to Apply"). Null when the posting has none, and then the page shows no deadline.
- `secondaryLocationNames` (array, optional): Additional locations, sorted as the page sorts them (its Location line reads primary then these, joined by "; "); empty when there are none.
- `compensationTierSummary` (string | null, optional): One-line pay range; null when the posting shows no pay.
- `compensationPhilosophyHtml` (string | null, optional): Note rendered under the pay section; null when absent.

## FAQ

### What does "Get Ashby job posting" do?

Read one Ashby job posting (jobs.ashbyhq.com/&lt;board&gt;/&lt;jobId&gt;), description HTML included.

### How do I automatically get Ashby job posting on jobs.ashbyhq.com?

Ask an AI agent connected to Reduck to run reduck/jobs.ashbyhq.com/get_job, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/jobs.ashbyhq.com/get_job

### Is there a jobs.ashbyhq.com API to get Ashby job posting?

You do not need one. "Get Ashby job posting" drives the real jobs.ashbyhq.com pages in a browser, so it works whether or not jobs.ashbyhq.com offers an API for this.

### What information do I need to provide?

Required: board, jobId.

### What does it return?

It returns id, title, teamNames, department, locationName, workplaceType, employmentType, descriptionHtml, compensationTiers, applicationDeadline, secondaryLocationNames, compensationTierSummary, compensationPhilosophyHtml.

### Do I need to be logged in to jobs.ashbyhq.com?

No. It only uses pages of jobs.ashbyhq.com that are reachable without signing in.

### Does it change anything on jobs.ashbyhq.com, or only read data?

Unknown: its author has not declared whether it changes anything on jobs.ashbyhq.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/jobs.ashbyhq.com/get_job, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/jobs.ashbyhq.com/get_job

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/jobs.ashbyhq.com/get_job
