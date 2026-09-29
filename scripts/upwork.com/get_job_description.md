# Get job description

Automatically get job description on upwork.com. Fetch a single Upwork job posting's full details by its ciphertext (the ~0… token in the job URL, returned by search_jobs). Covers title, full description, category, occupation, skills, budget or hourly range, workload and duration, experience level, screening questions and attachments. Also covers client activity (applicants, interviews, invites, hires) and the client: country, city, payment verified, member since, score and spend. Works signed out, so no Upwork account is needed; run it on the managed browser, since Upwork's Cloudflare check can block some paired browsers. A job that does not exist or was removed fails with a clear error. Read-only.

- Site: upwork.com
- Address: `reduck/upwork.com/get_job_description`
- Updated: 2026-09-28 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/upwork.com/get_job_description`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/upwork.com/get_job_description
```

## Input

- `ciphertext` (string, required): Upwork job ciphertext as it appears in the job URL — the segment after /jobs/, e.g. "~022067575483419247922". search_jobs returns it inside each job's url.

## Output

- `uid` (string, required): Numeric job id (ciphertext without the ~02 prefix).
- `url` (string, required)
- `title` (string, required)
- `ciphertext` (string, required): Job ciphertext (URL token), the caller's join key.
- `description` (string, required)
- `budget` (object | null, optional): Fixed-price budget. amount is 0 for hourly jobs.
- `client` (object, optional)
- `skills` (array, optional)
- `category` (object | null, optional)
- `postedOn` (string | null, optional)
- `workload` (string | null, optional): e.g. "Less than 30 hrs/week"; null on fixed-price jobs.
- `createdOn` (string | null, optional)
- `questions` (array, optional)
- `hideBudget` (boolean | null, optional)
- `occupation` (string | null, optional)
- `attachments` (array, optional)
- `publishTime` (string | null, optional)
- `hourlyBudget` (object, optional): Hourly rate range; min/max null and type NOT_PROVIDED when the client set no range.
- `categoryGroup` (object | null, optional)
- `clientActivity` (object | null, optional)
- `contractorTier` (number | null, optional): Experience level enum (1 entry, 2 intermediate, 3 expert).
- `qualifications` (object | null, optional)
- `isContractToHire` (boolean | null, optional)
- `engagementDuration` (object | null, optional)
- `numberOfPositionsToHire` (number | null, optional)

## FAQ

### What does "Get job description" do?

Fetch a single Upwork job posting's full details by its ciphertext (the ~0… token in the job URL, returned by search_jobs). Covers title, full description, category, occupation, skills, budget or hourly range, workload and duration, experience level, screening questions and attachments. Also covers client activity (applicants, interviews, invites, hires) and the client: country, city, payment verified, member since, score and spend. Works signed out, so no Upwork account is needed; run it on the managed browser, since Upwork's Cloudflare check can block some paired browsers. A job that does not exist or was removed fails with a clear error. Read-only.

### How do I automatically get job description on upwork.com?

Ask an AI agent connected to Reduck to run reduck/upwork.com/get_job_description, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/upwork.com/get_job_description

### Is there a upwork.com API to get job description?

You do not need one. "Get job description" drives the real upwork.com pages in a browser, so it works whether or not upwork.com offers an API for this.

### What information do I need to provide?

Required: ciphertext.

### What does it return?

It returns uid, url, title, budget, client, skills, category, postedOn, workload, createdOn, questions, ciphertext, hideBudget, occupation, attachments, description, publishTime, hourlyBudget, categoryGroup, clientActivity, contractorTier, qualifications, isContractToHire, engagementDuration, numberOfPositionsToHire.

### Do I need to be logged in to upwork.com?

No. It only uses pages of upwork.com that are reachable without signing in.

### Does it change anything on upwork.com, or only read data?

It only reads. It looks things up on upwork.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/upwork.com/get_job_description, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/upwork.com/get_job_description

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/upwork.com/get_job_description
