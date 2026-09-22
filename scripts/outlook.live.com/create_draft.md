# Create an Outlook.com email draft

Automatically create an Outlook.com email draft on outlook.live.com. Create a saved draft in Outlook.com (outlook.live.com) with a recipient, subject and body, without sending it. Returns the draft's row id, confirmed by reopening the Drafts folder and matching the text you supplied — never inferred from the composer. A malformed address is kept as typed rather than tokenised, and the draft still saves.

- Site: outlook.live.com
- Address: `reduck/outlook.live.com/create_draft`
- Updated: 2026-09-16 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/outlook.live.com/create_draft`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/create_draft
```

## Input

- `to` (string, required): Recipient email address, e.g. someone@example.com
- `body` (string, optional): Plain text body of the draft.
- `subject` (string, optional): Subject line of the draft.

## Output

- `to` (string, required)
- `subject` (string | null, required)
- `verified` (boolean, required): True only when the saved draft was found by reopening Drafts and matching caller-supplied text. Never inferred from the composer, and never satisfied by an unrelated existing draft.
- `body` (string | null, optional)
- `draftId` (string | null, optional): Row id of the saved draft in Drafts, usable with get_email. Null when no matching row was found.
- `composed` (object | null, optional): What the composer itself held just before saving. Distinguishes a fill failure from a save failure.
- `unverifiedReason` (string | null, optional): Why verification did not succeed, when it did not.

## FAQ

### What does "Create an Outlook.com email draft" do?

Create a saved draft in Outlook.com (outlook.live.com) with a recipient, subject and body, without sending it. Returns the draft's row id, confirmed by reopening the Drafts folder and matching the text you supplied — never inferred from the composer. A malformed address is kept as typed rather than tokenised, and the draft still saves.

### How do I automatically create an Outlook.com email draft on outlook.live.com?

Ask an AI agent connected to Reduck to run reduck/outlook.live.com/create_draft, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/create_draft

### Is there a outlook.live.com API to create an Outlook.com email draft?

You do not need one. "Create an Outlook.com email draft" drives the real outlook.live.com pages in a browser, so it works whether or not outlook.live.com offers an API for this.

### What information do I need to provide?

Required: to. Optional: body, subject.

### What does it return?

It returns to, body, draftId, subject, composed, verified, unverifiedReason.

### Do I need to be logged in to outlook.live.com?

Yes. It acts as you on outlook.live.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the outlook.live.com cookies saved by the Reduck extension.

### Does it change anything on outlook.live.com, or only read data?

It makes changes on outlook.live.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/outlook.live.com/create_draft, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/create_draft

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/outlook.live.com/create_draft
