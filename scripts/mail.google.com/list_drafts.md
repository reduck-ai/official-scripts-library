# List Gmail drafts

Automatically list Gmail drafts on mail.google.com. List the unsent drafts in the signed-in Gmail account, each with the identifier needed to open, edit or send it, plus its subject, preview text, whether it carries an attachment, and the date Gmail shows. Gmail's own draft total is returned alongside the number of drafts read, so a mailbox with more drafts than one screenful is visible as such rather than looking complete. An account with no drafts is a normal empty result, not an error. Note that the drafts list does not show who a draft is addressed to — Gmail puts the word "Draft" where the recipient would be — so recipients have to come from opening the draft itself.

- Site: mail.google.com
- Address: `reduck/mail.google.com/list_drafts`
- Updated: 2026-09-07 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mail.google.com/list_drafts`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mail.google.com/list_drafts
```

## Input

It takes no input.

## Output

- `drafts` (array, required)
- `returned` (number, required): How many drafts this read returned.
- `reportedTotal` (number | null, required): Total drafts as Gmail itself counts them next to the Drafts folder. Compare against `returned`: a larger figure means the mailbox holds more drafts than this screenful covers. Null when Gmail shows no count.

## FAQ

### What does "List Gmail drafts" do?

List the unsent drafts in the signed-in Gmail account, each with the identifier needed to open, edit or send it, plus its subject, preview text, whether it carries an attachment, and the date Gmail shows. Gmail's own draft total is returned alongside the number of drafts read, so a mailbox with more drafts than one screenful is visible as such rather than looking complete. An account with no drafts is a normal empty result, not an error. Note that the drafts list does not show who a draft is addressed to — Gmail puts the word "Draft" where the recipient would be — so recipients have to come from opening the draft itself.

### How do I automatically list Gmail drafts on mail.google.com?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/list_drafts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/list_drafts

### Is there a mail.google.com API to list Gmail drafts?

You do not need one. "List Gmail drafts" drives the real mail.google.com pages in a browser, so it works whether or not mail.google.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns drafts, returned, reportedTotal.

### Do I need to be logged in to mail.google.com?

Yes. It acts as you on mail.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mail.google.com cookies saved by the Reduck extension.

### Does it change anything on mail.google.com, or only read data?

It only reads. It looks things up on mail.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/list_drafts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/list_drafts

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/mail.google.com/list_drafts
