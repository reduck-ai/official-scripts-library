# Update a Gmail draft

Automatically update a Gmail draft on mail.google.com. Change the subject and/or body of an existing Gmail draft, identified by the id the drafts listing gives you. Whichever field you leave out keeps its current value; a field you pass replaces what was there rather than appending to it. The draft's current contents are read first, so asking for what it already says makes no change and says so. Gmail issues a draft a new id every time it is saved, so the id you passed in stops existing and the new one is returned — use that for any follow-up. The conversation id stays the same and is returned as the stable handle. Recipients are not touched by this script.

- Site: mail.google.com
- Address: `reduck/mail.google.com/update_draft`
- Updated: 2026-10-21 (v15)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mail.google.com/update_draft`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mail.google.com/update_draft
```

## Input

- `draftId` (string, required): The draft's current id, as returned by the drafts listing: a new message or a reply saved inside a conversation. Note Gmail replaces this id on every save, so use a freshly listed one.
- `body` (string, optional): Replacement body text. This replaces the whole body rather than adding to it; for a reply, the quoted message below the body stays as it is. Pass an empty string to clear it. Omit to leave the body as it is.
- `account` (string, optional): Google account email whose draft this is. Without it Gmail opens the first signed-in account (u/0), which may not be the one holding the draft when several accounts share the browser.
- `subject` (string, optional): Replacement subject line. Pass an empty string to clear it. Omit to leave the subject as it is. A reply's subject follows its conversation and cannot be changed: a different subject for a reply is refused and nothing is written.

## Output

- `after` (object, required): What the draft said after the edit, read back from the composer. For a reply, the body is the text above the quoted message.
- `before` (object, required): What the draft said before the edit. For a reply the subject is the one it carries from its conversation, and the body is the text above the quoted message.
- `changed` (array, required): Which fields were actually written. Empty when nothing needed changing.
- `draftId` (string, required): The draft's id AFTER the edit. Gmail mints a new one on every save, so this differs from the id passed in whenever something was written. Use this for follow-up calls.
- `account_used` (string, required): The Gmail account the draft was edited in, read from the session rather than assumed.
- `already_present` (boolean, required): True when the draft already said exactly what was asked for, so nothing was written.
- `verified_on_page` (boolean, required): True when Gmail confirmed the edit was saved: its answer to the save, or the Drafts list, shows the draft with the new subject and body under its new id.
- `isReply` (boolean, optional): True when the draft is a reply saved inside a conversation, false for a new message.
- `threadId` (string | null, optional): Id of the conversation holding the draft. Unlike the draft id this survives a save, which makes it the durable handle for the same draft over time.
- `verifiedBy` (string, optional): How the save was confirmed, when something was written: 'server' is Gmail's own answer to the save, which echoes the saved draft; 'drafts_list' is the draft found in the Drafts list under a new id with the new content, used when another Gmail tab in the browser saved it.
- `previousDraftId` (string, optional): The id that was passed in, which Gmail has now retired.

## FAQ

### What does "Update a Gmail draft" do?

Change the subject and/or body of an existing Gmail draft, identified by the id the drafts listing gives you. Whichever field you leave out keeps its current value; a field you pass replaces what was there rather than appending to it. The draft's current contents are read first, so asking for what it already says makes no change and says so. Gmail issues a draft a new id every time it is saved, so the id you passed in stops existing and the new one is returned — use that for any follow-up. The conversation id stays the same and is returned as the stable handle. Recipients are not touched by this script.

### How do I automatically update a Gmail draft on mail.google.com?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/update_draft, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/update_draft

### Is there a mail.google.com API to update a Gmail draft?

You do not need one. "Update a Gmail draft" drives the real mail.google.com pages in a browser, so it works whether or not mail.google.com offers an API for this.

### What information do I need to provide?

Required: draftId. Optional: body, account, subject.

### What does it return?

It returns after, before, changed, draftId, isReply, threadId, verifiedBy, account_used, already_present, previousDraftId, verified_on_page.

### Do I need to be logged in to mail.google.com?

Yes. It acts as you on mail.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mail.google.com cookies saved by the Reduck extension.

### Does it change anything on mail.google.com, or only read data?

It makes changes on mail.google.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/update_draft, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/update_draft

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/mail.google.com/update_draft
