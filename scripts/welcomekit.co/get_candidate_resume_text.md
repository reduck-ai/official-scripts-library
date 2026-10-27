# Get Welcome to the Jungle candidate CV text

Automatically get Welcome to the Jungle candidate CV text on welcomekit.co. Read the text of a Welcome to the Jungle ATS candidate's CV, without downloading a file, so many CVs can be screened in parallel. Returns the text and page count, or hasResume false when the candidate attached no CV. Only PDF CVs can be read: another format (such as Word) gives an error naming it, and a scanned PDF with no text layer returns empty text.

- Site: welcomekit.co
- Address: `reduck/welcomekit.co/get_candidate_resume_text`
- Updated: 2026-10-22 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/welcomekit.co/get_candidate_resume_text`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/get_candidate_resume_text
```

## Input

- `org` (string, required): Organization reference as it appears in your dashboard URL https://www.welcomekit.co/dashboard/o/<org>/ (6-char code)
- `candidateReference` (string, required): Candidate reference from list_job_candidates or search_all_candidates, format: <orgprefix>-<24 hex chars>

## Output

- `hasResume` (boolean, required): false when the candidate attached no CV; the other fields are then null
- `candidateReference` (string, required)
- `text` (string | null, optional): CV text, pages separated by a blank line. Empty string for a scanned PDF with no text layer.
- `pageCount` (integer | null, optional)
- `contentType` (string | null, optional)

## FAQ

### What does "Get Welcome to the Jungle candidate CV text" do?

Read the text of a Welcome to the Jungle ATS candidate's CV, without downloading a file, so many CVs can be screened in parallel. Returns the text and page count, or hasResume false when the candidate attached no CV. Only PDF CVs can be read: another format (such as Word) gives an error naming it, and a scanned PDF with no text layer returns empty text.

### How do I automatically get Welcome to the Jungle candidate CV text on welcomekit.co?

Ask an AI agent connected to Reduck to run reduck/welcomekit.co/get_candidate_resume_text, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/get_candidate_resume_text

### Is there a welcomekit.co API to get Welcome to the Jungle candidate CV text?

You do not need one. "Get Welcome to the Jungle candidate CV text" drives the real welcomekit.co pages in a browser, so it works whether or not welcomekit.co offers an API for this.

### What information do I need to provide?

Required: org, candidateReference.

### What does it return?

It returns text, hasResume, pageCount, contentType, candidateReference.

### Do I need to be logged in to welcomekit.co?

Yes. It acts as you on welcomekit.co: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the welcomekit.co cookies saved by the Reduck extension.

### Does it change anything on welcomekit.co, or only read data?

It only reads. It looks things up on welcomekit.co and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/welcomekit.co/get_candidate_resume_text, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/get_candidate_resume_text

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/welcomekit.co/get_candidate_resume_text
