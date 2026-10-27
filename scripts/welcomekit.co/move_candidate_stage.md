# Move a Welcome to the Jungle (WelcomeKit) candidate to another stage

Automatically move a Welcome to the Jungle (WelcomeKit) candidate to another stage on welcomekit.co. Move a Welcome to the Jungle ATS candidate to another stage of their job's pipeline, given the stage id from list_job_candidates. Returns the stage the candidate left and the one they are now in, read back from the site after the move. An id that is not one of the job's stages fails with the job's list of stages.

- Site: welcomekit.co
- Address: `reduck/welcomekit.co/move_candidate_stage`
- Updated: 2026-10-22 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/welcomekit.co/move_candidate_stage`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/move_candidate_stage
```

## Input

- `org` (string, required): Organization reference as it appears in your dashboard URL https://www.welcomekit.co/dashboard/o/<org>/ (6-char code).
- `stageId` (integer, required): Target stage id: the id of one of the job's stages as list_job_candidates returns them.
- `candidateReference` (string, required): Candidate reference from list_job_candidates, format: <orgprefix>-<24 hex chars>

## Output

- `toStageId` (integer, required)
- `candidateReference` (string, required)
- `toStage` (string | null, optional)
- `fromStage` (string | null, optional)
- `updatedAt` (string | null, optional)
- `fromStageId` (integer | null, optional)
- `jobReference` (string | null, optional)

## FAQ

### What does "Move a Welcome to the Jungle (WelcomeKit) candidate to another stage" do?

Move a Welcome to the Jungle ATS candidate to another stage of their job's pipeline, given the stage id from list_job_candidates. Returns the stage the candidate left and the one they are now in, read back from the site after the move. An id that is not one of the job's stages fails with the job's list of stages.

### How do I automatically move a Welcome to the Jungle (WelcomeKit) candidate to another stage on welcomekit.co?

Ask an AI agent connected to Reduck to run reduck/welcomekit.co/move_candidate_stage, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/move_candidate_stage

### Is there a welcomekit.co API to move a Welcome to the Jungle (WelcomeKit) candidate to another stage?

You do not need one. "Move a Welcome to the Jungle (WelcomeKit) candidate to another stage" drives the real welcomekit.co pages in a browser, so it works whether or not welcomekit.co offers an API for this.

### What information do I need to provide?

Required: org, candidateReference, stageId.

### What does it return?

It returns toStage, fromStage, toStageId, updatedAt, fromStageId, jobReference, candidateReference.

### Do I need to be logged in to welcomekit.co?

Yes. It acts as you on welcomekit.co: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the welcomekit.co cookies saved by the Reduck extension.

### Does it change anything on welcomekit.co, or only read data?

It makes changes on welcomekit.co, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/welcomekit.co/move_candidate_stage, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/move_candidate_stage

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/welcomekit.co/move_candidate_stage
