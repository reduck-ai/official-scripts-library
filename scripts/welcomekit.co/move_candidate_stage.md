# Move ATS candidate stage

Automatically move ATS candidate stage on welcomekit.co. Move an ATS candidate to another pipeline stage by stage id or label (built-in ref, UI alias, or custom column name). Returns from/to stages, and verifies the move actually applied.

- Site: welcomekit.co
- Address: `reduck/welcomekit.co/move_candidate_stage`
- Updated: 2026-08-27 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/welcomekit.co/move_candidate_stage`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/move_candidate_stage
```

## Input

- `org` (string, required): Organization reference as it appears in your dashboard URL https://www.welcomekit.co/dashboard/o/<org>/ (6-char code).
- `candidateReference` (string, required): Candidate reference from list_candidates, format: <orgprefix>-<24 hex chars>
- `stage` (string, optional): Target stage as label: built-in reference (initial, to_refuse, refused, to_meet, interviewed, made_offer, hired), UI alias (New, Rejected, Awaiting Rejection, Offer) or custom column name (e.g. Test sent). Case-insensitive.
- `stageId` (integer, optional): Target stage id (from list_jobs/list_candidates stages). Wins over stage when both given.

## Output

- `toStageId` (integer, required)
- `candidateReference` (string, required)
- `toStage` (string | null, optional)
- `fromStage` (string | null, optional)
- `updatedAt` (string | null, optional)
- `fromStageId` (integer | null, optional)
- `jobReference` (string | null, optional)

## FAQ

### What does "Move ATS candidate stage" do?

Move an ATS candidate to another pipeline stage by stage id or label (built-in ref, UI alias, or custom column name). Returns from/to stages, and verifies the move actually applied.

### How do I automatically move ATS candidate stage on welcomekit.co?

Ask an AI agent connected to Reduck to run reduck/welcomekit.co/move_candidate_stage, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/move_candidate_stage

### Is there a welcomekit.co API to move ATS candidate stage?

You do not need one. "Move ATS candidate stage" drives the real welcomekit.co pages in a browser, so it works whether or not welcomekit.co offers an API for this.

### What information do I need to provide?

Required: org, candidateReference. Optional: stage, stageId.

### What does it return?

It returns toStage, fromStage, toStageId, updatedAt, fromStageId, jobReference, candidateReference.

### Do I need to be logged in to welcomekit.co?

Yes. It acts as you on welcomekit.co: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the welcomekit.co cookies saved by the Reduck extension.

### Does it change anything on welcomekit.co, or only read data?

It makes changes on welcomekit.co, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/welcomekit.co/move_candidate_stage, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/move_candidate_stage

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/welcomekit.co/move_candidate_stage
