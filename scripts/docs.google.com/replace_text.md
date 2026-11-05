# Google Docs: find and replace text

Automatically find and replace text on docs.google.com. Find and replace text in a Google Doc you can edit, directly (not as suggestions), with Docs' own Find and replace. Each find/replace pair is applied in order to every match; matching is literal and case-sensitive by default, and accents count. Returns the matches found per pair and reads the document back to confirm. An empty replace deletes the matches. Use dryRun to count matches without changing anything. When the browser is signed in to several Google accounts, pass the account to act as.

- Site: docs.google.com
- Address: `reduck/docs.google.com/replace_text`
- Updated: 2026-11-04 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/docs.google.com/replace_text`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/docs.google.com/replace_text
```

## Input

- `url` (string, required): Link to the Google Doc (https://docs.google.com/document/d/<id>/...) or the bare document id.
- `replacements` (array, required): Applied in order.
- `dryRun` (boolean, optional): Count matches only; nothing is changed.
- `account` (string, optional): Google account to act as when the browser is signed in to several. The run stops if the editor is signed in as someone else.
- `matchCase` (boolean, optional): Case-sensitive matching (default true).

## Output

- `dryRun` (boolean, required)
- `verified` (boolean | null, required): True when, read back, no applied find text is left (where its replacement does not contain it); null on a dry run or when nothing matched.
- `documentId` (string, required)
- `accountUsed` (string | null, required): Email of the Google account the editor was signed in as.
- `replacements` (array, required)
- `totalMatches` (integer, required)

## FAQ

### What does "Google Docs: find and replace text" do?

Find and replace text in a Google Doc you can edit, directly (not as suggestions), with Docs' own Find and replace. Each find/replace pair is applied in order to every match; matching is literal and case-sensitive by default, and accents count. Returns the matches found per pair and reads the document back to confirm. An empty replace deletes the matches. Use dryRun to count matches without changing anything. When the browser is signed in to several Google accounts, pass the account to act as.

### How do I automatically find and replace text on docs.google.com?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/replace_text, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/replace_text

### Is there a docs.google.com API to find and replace text?

You do not need one. "Google Docs: find and replace text" drives the real docs.google.com pages in a browser, so it works whether or not docs.google.com offers an API for this.

### What information do I need to provide?

Required: url, replacements. Optional: dryRun, account, matchCase.

### What does it return?

It returns dryRun, verified, documentId, accountUsed, replacements, totalMatches.

### Do I need to be logged in to docs.google.com?

Yes. It acts as you on docs.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the docs.google.com cookies saved by the Reduck extension.

### Does it change anything on docs.google.com, or only read data?

It makes changes on docs.google.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/replace_text, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/replace_text

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/docs.google.com/replace_text
