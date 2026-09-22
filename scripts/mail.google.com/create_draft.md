# Create a Gmail draft

Automatically create a Gmail draft on mail.google.com. Compose a Gmail message and save it as a draft without sending it. Takes to/cc/bcc, subject and body, and confirms the draft exists in Drafts afterward rather than trusting the compose window closing.

- Site: mail.google.com
- Address: `reduck/mail.google.com/create_draft`
- Updated: 2026-08-27 (v24)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mail.google.com/create_draft`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mail.google.com/create_draft
```

## Input

- `to` (array, required): Recipient email address(es).
- `body` (string, required): Plain-text body.
- `subject` (string, required): Subject line.
- `cc` (array, optional): Optional Cc addresses.
- `bcc` (array, optional): Optional Bcc addresses.
- `account` (string, optional): Google account email to act as (authuser=). Without it Gmail picks u/0, nondeterministic in a multi-account jar.

## Output

- `status` (string, required)
- `subject` (string, required)
- `verifiedInDrafts` (boolean, required)
- `to` (array, optional)
- `verifiedBy` (string, optional): How existence was confirmed. 'count' means the subject could not be matched textually (e.g. Gmail renders emoji as images) but the Drafts count rose by exactly one.
- `draftsCountAfter` (integer | null, optional)
- `draftsCountBefore` (integer | null, optional)

## FAQ

### What does "Create a Gmail draft" do?

Compose a Gmail message and save it as a draft without sending it. Takes to/cc/bcc, subject and body, and confirms the draft exists in Drafts afterward rather than trusting the compose window closing.

### How do I automatically create a Gmail draft on mail.google.com?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/create_draft, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/create_draft

### Is there a mail.google.com API to create a Gmail draft?

You do not need one. "Create a Gmail draft" drives the real mail.google.com pages in a browser, so it works whether or not mail.google.com offers an API for this.

### What information do I need to provide?

Required: to, subject, body. Optional: cc, bcc, account.

### What does it return?

It returns to, status, subject, verifiedBy, draftsCountAfter, verifiedInDrafts, draftsCountBefore.

### Do I need to be logged in to mail.google.com?

Yes. It acts as you on mail.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mail.google.com cookies saved by the Reduck extension.

### Does it change anything on mail.google.com, or only read data?

It makes changes on mail.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/create_draft, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/create_draft

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/mail.google.com/create_draft
