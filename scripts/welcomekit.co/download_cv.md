# Download candidate CV

Automatically download candidate CV on welcomekit.co. Download a candidate's CV (resume PDF) from the ATS to a local file on the agent machine. Returns path, filename, size, contentType, and hasResume. Gotcha: hasResume=false (path/filename null) when the candidate attached no CV; the signed resume URL is re-fetched fresh each run.

- Site: welcomekit.co
- Address: `reduck/welcomekit.co/download_cv`
- Updated: 2026-09-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/welcomekit.co/download_cv`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/download_cv
```

## Input

- `org` (string, required): REQUIRED. Organization reference as it appears in your dashboard URL https://www.welcomekit.co/dashboard/o/<org>/ (6-char code)
- `candidateReference` (string, required): Candidate reference from list_candidates, format: reduc-<24 hex chars>

## Output

- `hasResume` (boolean, required): false = the candidate attached no CV (path/filename null)
- `candidateReference` (string, required)
- `path` (string | null, optional): Local path on the agent machine (/tmp/reduck-downloads/...)
- `size` (integer | null, optional): Size in bytes as reported by the ATS
- `filename` (string | null, optional)
- `contentType` (string | null, optional)

## FAQ

### What does "Download candidate CV" do?

Download a candidate's CV (resume PDF) from the ATS to a local file on the agent machine. Returns path, filename, size, contentType, and hasResume. Gotcha: hasResume=false (path/filename null) when the candidate attached no CV; the signed resume URL is re-fetched fresh each run.

### How do I automatically download candidate CV on welcomekit.co?

Ask an AI agent connected to Reduck to run reduck/welcomekit.co/download_cv, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/download_cv

### Is there a welcomekit.co API to download candidate CV?

You do not need one. "Download candidate CV" drives the real welcomekit.co pages in a browser, so it works whether or not welcomekit.co offers an API for this.

### What information do I need to provide?

Required: candidateReference, org.

### What does it return?

It returns path, size, filename, hasResume, contentType, candidateReference.

### Do I need to be logged in to welcomekit.co?

Yes. It acts as you on welcomekit.co: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the welcomekit.co cookies saved by the Reduck extension.

### Does it change anything on welcomekit.co, or only read data?

It makes changes on welcomekit.co, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/welcomekit.co/download_cv, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/download_cv

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/welcomekit.co/download_cv
