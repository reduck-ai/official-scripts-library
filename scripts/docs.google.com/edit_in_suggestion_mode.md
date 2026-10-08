# Google Docs: suggest edits (find and replace in Suggesting mode)

Automatically suggest edits (find and replace in Suggesting mode) on docs.google.com. Edit an existing Google Doc in Suggesting mode: each find/replace pair becomes a tracked suggestion the owner can accept or reject, rather than a direct edit. Returns, per pair, how many matches were found and whether a suggestion was created, plus the Google account that made the suggestions. Matching is literal and case-sensitive by default. Accents count, so "café" does not match "cafe". Use dryRun to count matches without changing anything. Needs comment or edit access to the document.

- Site: docs.google.com
- Address: `reduck/docs.google.com/edit_in_suggestion_mode`
- Updated: 2026-10-07 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/docs.google.com/edit_in_suggestion_mode`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/docs.google.com/edit_in_suggestion_mode
```

## Input

- `url` (string, required): Link to the Google Doc (https://docs.google.com/document/d/<id>/...) or the bare document id.
- `replacements` (array, required): Applied in order. Each pair becomes one suggestion covering all its matches.
- `dryRun` (boolean, optional): Count matches only; no suggestion is created.
- `account` (string, optional): Google account email to act as when the browser has several Google accounts signed in. The run stops if the editor is signed in as someone else.
- `matchCase` (boolean, optional): Case-sensitive matching (default true).

## Output

- `dryRun` (boolean, required)
- `documentId` (string, required)
- `accountUsed` (string, required): Email of the Google account the suggestions are attributed to, read from the editor.
- `replacements` (array, required)
- `totalMatches` (integer, required)
- `suggestionsCreated` (integer, required)
- `matchCase` (boolean, optional)
- `verifiedAfterReload` (boolean | null, optional): True when the new suggestions were still there after reopening the document; null when nothing was applied.

## FAQ

### What does "Google Docs: suggest edits (find and replace in Suggesting mode)" do?

Edit an existing Google Doc in Suggesting mode: each find/replace pair becomes a tracked suggestion the owner can accept or reject, rather than a direct edit. Returns, per pair, how many matches were found and whether a suggestion was created, plus the Google account that made the suggestions. Matching is literal and case-sensitive by default. Accents count, so "café" does not match "cafe". Use dryRun to count matches without changing anything. Needs comment or edit access to the document.

### How do I automatically suggest edits (find and replace in Suggesting mode) on docs.google.com?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/edit_in_suggestion_mode, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/edit_in_suggestion_mode

### Is there a docs.google.com API to suggest edits (find and replace in Suggesting mode)?

You do not need one. "Google Docs: suggest edits (find and replace in Suggesting mode)" drives the real docs.google.com pages in a browser, so it works whether or not docs.google.com offers an API for this.

### What information do I need to provide?

Required: url, replacements. Optional: dryRun, account, matchCase.

### What does it return?

It returns dryRun, matchCase, documentId, accountUsed, replacements, totalMatches, suggestionsCreated, verifiedAfterReload.

### Do I need to be logged in to docs.google.com?

Yes. It acts as you on docs.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the docs.google.com cookies saved by the Reduck extension.

### Does it change anything on docs.google.com, or only read data?

It makes changes on docs.google.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/edit_in_suggestion_mode, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/edit_in_suggestion_mode

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/docs.google.com/edit_in_suggestion_mode
