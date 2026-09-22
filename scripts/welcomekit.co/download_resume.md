# Download candidate resume

Automatically download candidate resume on welcomekit.co. Download a candidate's CV (resume PDF) from the ATS to a local file on the agent machine. Returns path, filename, size, contentType, and hasResume, which is false (with path/filename null) when the candidate attached no CV; the signed resume URL is re-fetched fresh on every run. Because the extension device runs a single shared browser page, call this one candidate at a time rather than in a parallel batch, which can misattribute a download to the wrong candidate.

- Site: welcomekit.co
- Address: `reduck/welcomekit.co/download_resume`
- Updated: 2026-09-11 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/welcomekit.co/download_resume`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/download_resume
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

### What does "Download candidate resume" do?

Download a candidate's CV (resume PDF) from the ATS to a local file on the agent machine. Returns path, filename, size, contentType, and hasResume, which is false (with path/filename null) when the candidate attached no CV; the signed resume URL is re-fetched fresh on every run. Because the extension device runs a single shared browser page, call this one candidate at a time rather than in a parallel batch, which can misattribute a download to the wrong candidate.

### How do I automatically download candidate resume on welcomekit.co?

Ask an AI agent connected to Reduck to run reduck/welcomekit.co/download_resume, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/download_resume

### Is there a welcomekit.co API to download candidate resume?

You do not need one. "Download candidate resume" drives the real welcomekit.co pages in a browser, so it works whether or not welcomekit.co offers an API for this.

### What information do I need to provide?

Required: candidateReference, org.

### What does it return?

It returns path, size, filename, hasResume, contentType, candidateReference.

### Do I need to be logged in to welcomekit.co?

Yes. It acts as you on welcomekit.co: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the welcomekit.co cookies saved by the Reduck extension.

### Does it change anything on welcomekit.co, or only read data?

It only reads. It looks things up on welcomekit.co and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/welcomekit.co/download_resume, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/download_resume

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/welcomekit.co/download_resume
