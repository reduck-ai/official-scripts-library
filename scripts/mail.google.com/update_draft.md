# Update a Gmail draft

Automatically update a Gmail draft on mail.google.com. Change the subject and/or body of an existing Gmail draft, identified by the id the drafts listing gives you. Whichever field you leave out keeps its current value; a field you pass replaces what was there rather than appending to it. The draft's current contents are read first, so asking for what it already says makes no change and says so. Gmail issues a draft a new id every time it is saved, so the id you passed in stops existing and the new one is returned — use that for any follow-up. The conversation id stays the same and is returned as the stable handle. Recipients are not touched by this script.

- Site: mail.google.com
- Address: `reduck/mail.google.com/update_draft`
- Updated: 2026-09-07 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mail.google.com/update_draft`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mail.google.com/update_draft
```

## Input

- `draftId` (string, required): The draft's current id, as returned by the drafts listing. Note Gmail replaces this id on every save, so use a freshly listed one.
- `body` (string, optional): Replacement body text. This replaces the whole body rather than adding to it. Pass an empty string to clear it. Omit to leave the body as it is.
- `subject` (string, optional): Replacement subject line. Pass an empty string to clear it. Omit to leave the subject as it is.

## Output

- `after` (object, required): What the draft said after the edit, read back from the composer.
- `before` (object, required): What the draft said before the edit.
- `changed` (array, required): Which fields were actually written. Empty when nothing needed changing.
- `draftId` (string, required): The draft's id AFTER the edit. Gmail mints a new one on every save, so this differs from the id passed in whenever something was written. Use this for follow-up calls.
- `account_used` (string, required): The Gmail account the draft was edited in, read from the session rather than assumed.
- `already_present` (boolean, required): True when the draft already said exactly what was asked for, so nothing was written.
- `verified_on_page` (boolean, required): True when the drafts listing showed the draft with the new subject — and, when the body changed, with the new body in its preview — after Gmail saved it.
- `threadId` (string | null, optional): Id of the conversation holding the draft. Unlike the draft id this survives a save, which makes it the durable handle for the same draft over time.
- `previousDraftId` (string, optional): The id that was passed in, which Gmail has now retired.

## FAQ

### What does "Update a Gmail draft" do?

Change the subject and/or body of an existing Gmail draft, identified by the id the drafts listing gives you. Whichever field you leave out keeps its current value; a field you pass replaces what was there rather than appending to it. The draft's current contents are read first, so asking for what it already says makes no change and says so. Gmail issues a draft a new id every time it is saved, so the id you passed in stops existing and the new one is returned — use that for any follow-up. The conversation id stays the same and is returned as the stable handle. Recipients are not touched by this script.

### How do I automatically update a Gmail draft on mail.google.com?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/update_draft, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/update_draft

### Is there a mail.google.com API to update a Gmail draft?

You do not need one. "Update a Gmail draft" drives the real mail.google.com pages in a browser, so it works whether or not mail.google.com offers an API for this.

### What information do I need to provide?

Required: draftId. Optional: body, subject.

### What does it return?

It returns after, before, changed, draftId, threadId, account_used, already_present, previousDraftId, verified_on_page.

### Do I need to be logged in to mail.google.com?

Yes. It acts as you on mail.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mail.google.com cookies saved by the Reduck extension.

### Does it change anything on mail.google.com, or only read data?

It makes changes on mail.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/update_draft, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/update_draft

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/mail.google.com/update_draft
