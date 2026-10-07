# Create candidate review

Automatically create candidate review on welcomekit.co. Add a review (evaluation) to a Welcome to the Jungle (Welcome Kit) ATS candidate, posted as the logged-in recruiter. The comment is plain text; reviewNotes (per-criterion scores) stays empty unless the job has evaluation criteria configured. Returns the created review (id, comment, rawComment, reviewNotes, createdAt); delete it via its id.

- Site: welcomekit.co
- Address: `reduck/welcomekit.co/create_review`
- Updated: 2026-10-06 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/welcomekit.co/create_review`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/create_review
```

## Input

- `org` (string, required): Organization reference from your dashboard URL https://www.welcomekit.co/dashboard/o/<org>/ (6-char code, e.g. abc123).
- `comment` (string, required): Review text, plain text.
- `candidateReference` (string, required): Candidate reference from list_job_candidates.

## Output

- `id` (integer, required): Review id.
- `candidateId` (integer | null, required): Numeric candidate id.
- `user` (object | null, optional)
- `jobId` (integer | null, optional)
- `comment` (string | null, optional): Review text as saved.
- `createdAt` (string | null, optional)
- `rawComment` (string | null, optional): Review text without formatting.
- `averageNote` (number | null, optional)
- `reviewNotes` (array, optional): Per-criterion scores; empty unless the job has evaluation criteria.

## FAQ

### What does "Create candidate review" do?

Add a review (evaluation) to a Welcome to the Jungle (Welcome Kit) ATS candidate, posted as the logged-in recruiter. The comment is plain text; reviewNotes (per-criterion scores) stays empty unless the job has evaluation criteria configured. Returns the created review (id, comment, rawComment, reviewNotes, createdAt); delete it via its id.

### How do I automatically create candidate review on welcomekit.co?

Ask an AI agent connected to Reduck to run reduck/welcomekit.co/create_review, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/create_review

### Is there a welcomekit.co API to create candidate review?

You do not need one. "Create candidate review" drives the real welcomekit.co pages in a browser, so it works whether or not welcomekit.co offers an API for this.

### What information do I need to provide?

Required: org, candidateReference, comment.

### What does it return?

It returns id, user, jobId, comment, createdAt, rawComment, averageNote, candidateId, reviewNotes.

### Do I need to be logged in to welcomekit.co?

Yes. It acts as you on welcomekit.co: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the welcomekit.co cookies saved by the Reduck extension.

### Does it change anything on welcomekit.co, or only read data?

It makes changes on welcomekit.co, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/welcomekit.co/create_review, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/create_review

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/welcomekit.co/create_review
