# List job candidates

Automatically list job candidates on welcomekit.co. List all candidates of one ATS job. Returns candidates (reference, name, email, phone, linkedin, stage, votes, resumeUrl, dates) and the job's stages. reference is the join key for get_candidate and download_cv.

- Site: welcomekit.co
- Address: `reduck/welcomekit.co/list_candidates`
- Updated: 2026-09-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/welcomekit.co/list_candidates`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/list_candidates
```

## Input

- `org` (string, required): Organization reference as it appears in your dashboard URL https://www.welcomekit.co/dashboard/o/<org>/ (6-char code).
- `jobReference` (string, required): Job reference from list_jobs, format: <ORGPREFIX>_<7 alphanumeric>
- `page` (integer, optional)
- `perPage` (integer, optional)

## Output

- `stages` (array, required): The job's pipeline columns (stage_id join key)
- `candidates` (array, required)
- `jobReference` (string, required)
- `org` (string, optional)
- `page` (integer, optional)
- `jobName` (string | null, optional)
- `perPage` (integer, optional)

## FAQ

### What does "List job candidates" do?

List all candidates of one ATS job. Returns candidates (reference, name, email, phone, linkedin, stage, votes, resumeUrl, dates) and the job's stages. reference is the join key for get_candidate and download_cv.

### How do I automatically list job candidates on welcomekit.co?

Ask an AI agent connected to Reduck to run reduck/welcomekit.co/list_candidates, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/list_candidates

### Is there a welcomekit.co API to list job candidates?

You do not need one. "List job candidates" drives the real welcomekit.co pages in a browser, so it works whether or not welcomekit.co offers an API for this.

### What information do I need to provide?

Required: jobReference, org. Optional: page, perPage.

### What does it return?

It returns org, page, stages, jobName, perPage, candidates, jobReference.

### Do I need to be logged in to welcomekit.co?

Yes. It acts as you on welcomekit.co: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the welcomekit.co cookies saved by the Reduck extension.

### Does it change anything on welcomekit.co, or only read data?

It only reads. It looks things up on welcomekit.co and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/welcomekit.co/list_candidates, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/list_candidates

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/welcomekit.co/list_candidates
