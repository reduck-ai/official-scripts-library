# Get candidate full profile

Automatically get candidate full profile on welcomekit.co. Get a candidate's full ATS profile card by their candidate reference. Returns profile and socials, cover letter, emails exchanged, event timeline, screening answers, votes, reviews, documents, other applications, and hiring/rejection fields. resumeUrl is a signed URL that expires after about 2 hours, so re-fetch it rather than storing it.

- Site: welcomekit.co
- Address: `reduck/welcomekit.co/get_candidate`
- Updated: 2026-10-06 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/welcomekit.co/get_candidate`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/get_candidate
```

## Input

- `org` (string, required): Organization reference as it appears in your dashboard URL https://www.welcomekit.co/dashboard/o/<org>/ (6-char code)
- `candidateReference` (string, required): Candidate reference from list_job_candidates, format: <orgprefix>-<24 hex chars>

## Output

- `reference` (string, required)
- `jobReference` (string | null, required)
- `tags` (array, optional)
- `jobId` (integer | null, optional)
- `votes` (array, optional)
- `emails` (array, optional)
- `events` (array, optional)
- `origin` (string | null, optional)
- `salary` (string | null, optional)
- `answers` (array, optional)
- `profile` (object, optional)
- `reviews` (array, optional)
- `stageId` (integer | null, optional)
- `archived` (boolean | null, optional)
- `referrer` (string | null, optional)
- `createdAt` (string | null, optional)
- `documents` (array, optional)
- `resumeUrl` (string | null, optional): Signed CDN URL (expires after ~2h — re-fetch rather than store)
- `hiringDate` (string | null, optional)
- `nbComments` (integer | null, optional)
- `resumeSize` (integer | null, optional)
- `coverLetter` (string | null, optional)
- `nbSentEmails` (integer | null, optional)
- `portfolioUrl` (string | null, optional)
- `startingDate` (string | null, optional)
- `lastActivityAt` (string | null, optional)
- `rejectedReason` (string | null, optional)
- `otherApplications` (array, optional)

## FAQ

### What does "Get candidate full profile" do?

Get a candidate's full ATS profile card by their candidate reference. Returns profile and socials, cover letter, emails exchanged, event timeline, screening answers, votes, reviews, documents, other applications, and hiring/rejection fields. resumeUrl is a signed URL that expires after about 2 hours, so re-fetch it rather than storing it.

### How do I automatically get candidate full profile on welcomekit.co?

Ask an AI agent connected to Reduck to run reduck/welcomekit.co/get_candidate, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/get_candidate

### Is there a welcomekit.co API to get candidate full profile?

You do not need one. "Get candidate full profile" drives the real welcomekit.co pages in a browser, so it works whether or not welcomekit.co offers an API for this.

### What information do I need to provide?

Required: candidateReference, org.

### What does it return?

It returns tags, jobId, votes, emails, events, origin, salary, answers, profile, reviews, stageId, archived, referrer, createdAt, documents, reference, resumeUrl, hiringDate, nbComments, resumeSize, coverLetter, jobReference, nbSentEmails, portfolioUrl, startingDate, lastActivityAt, rejectedReason, otherApplications.

### Do I need to be logged in to welcomekit.co?

Yes. It acts as you on welcomekit.co: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the welcomekit.co cookies saved by the Reduck extension.

### Does it change anything on welcomekit.co, or only read data?

It only reads. It looks things up on welcomekit.co and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/welcomekit.co/get_candidate, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/get_candidate

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/welcomekit.co/get_candidate
