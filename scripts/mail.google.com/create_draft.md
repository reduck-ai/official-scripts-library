# Create a Gmail draft

Automatically create a Gmail draft on mail.google.com. Compose a Gmail message and save it as a draft without sending it. Takes to/cc/bcc, a subject and a plain-text body, and can put one of the account's Gmail signatures under the body by its name, or none; without that choice the draft keeps Gmail's default signature for new emails. Reports success only once Gmail confirms the draft is saved under Drafts with that subject and body, and returns the account used, the draft id that update_draft and send_draft take, and the id of its conversation. Create drafts one after another on a browser: several at once can leave Gmail without saving some of them, which the call reports as an error.

- Site: mail.google.com
- Address: `reduck/mail.google.com/create_draft`
- Updated: 2026-10-21 (v39)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mail.google.com/create_draft`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mail.google.com/create_draft
```

## Input

- `to` (any, required): Recipient email address(es). A single string or an array of strings.
- `body` (string, required): Plain-text body.
- `subject` (string, required): Subject line.
- `cc` (any, optional): Optional Cc address(es). A single string or an array of strings.
- `bcc` (any, optional): Optional Bcc address(es). A single string or an array of strings.
- `account` (string, optional): Google account email to act as (authuser=). Without it Gmail picks u/0, nondeterministic in a multi-account jar.
- `signature` (string, optional): Name of one of the account's Gmail signatures to put under the body, as Gmail lists it in the composer's signature menu. An empty string means no signature. Omit it to keep what Gmail puts in a new message: the account's default signature for new emails, if one is set.

## Output

- `status` (string, required)
- `subject` (string, required)
- `verifiedInDrafts` (boolean, required): True when Gmail confirmed the draft is saved under Drafts with this subject and body.
- `cc` (array, optional)
- `to` (array, optional)
- `bcc` (array, optional)
- `account` (string | null, optional): The Gmail account the draft was saved in, as the compose window names it.
- `draftId` (string | null, optional): Gmail's id for the saved draft, the one the drafts listing returns and update_draft and send_draft take. Gmail replaces it whenever the draft is saved again.
- `threadId` (string | null, optional): Id of the conversation holding the draft. It stays the same when the draft is saved again.
- `signature` (string | null, optional): The signature chosen for this draft, by the name Gmail lists it under; an empty string when no signature was asked for; null when the call left Gmail's default in place.
- `verifiedBy` (string, optional): How the save was confirmed: 'server' is Gmail's own answer to the save, which echoes the saved draft; 'drafts_list' is the draft found in the Drafts list with this subject and body, used when another Gmail tab in the browser saved it.
- `hasSignature` (boolean, optional): Whether the saved draft carries a signature under the body.

## FAQ

### What does "Create a Gmail draft" do?

Compose a Gmail message and save it as a draft without sending it. Takes to/cc/bcc, a subject and a plain-text body, and can put one of the account's Gmail signatures under the body by its name, or none; without that choice the draft keeps Gmail's default signature for new emails. Reports success only once Gmail confirms the draft is saved under Drafts with that subject and body, and returns the account used, the draft id that update_draft and send_draft take, and the id of its conversation. Create drafts one after another on a browser: several at once can leave Gmail without saving some of them, which the call reports as an error.

### How do I automatically create a Gmail draft on mail.google.com?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/create_draft, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/create_draft

### Is there a mail.google.com API to create a Gmail draft?

You do not need one. "Create a Gmail draft" drives the real mail.google.com pages in a browser, so it works whether or not mail.google.com offers an API for this.

### What information do I need to provide?

Required: to, subject, body. Optional: cc, bcc, account, signature.

### What does it return?

It returns cc, to, bcc, status, account, draftId, subject, threadId, signature, verifiedBy, hasSignature, verifiedInDrafts.

### Do I need to be logged in to mail.google.com?

Yes. It acts as you on mail.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mail.google.com cookies saved by the Reduck extension.

### Does it change anything on mail.google.com, or only read data?

It makes changes on mail.google.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/create_draft, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/create_draft

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/mail.google.com/create_draft
