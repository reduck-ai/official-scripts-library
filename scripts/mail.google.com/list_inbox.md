# List Gmail inbox

Automatically list Gmail inbox on mail.google.com. List the messages on the first page of the Gmail inbox. Requires an authenticated mail.google.com session. Returns folder, total (the range line as rendered, e.g. "1–50 of 240") and rows of sender, subject, snippet, date plus the unread / starred / hasAttachment flags. Covers only the first inbox page (up to ~50 rows as Gmail renders it); there is no pagination. Be aware that the output requires at least one row, so a genuinely empty inbox is not representable and will surface as a failure rather than an empty list.

- Site: mail.google.com
- Address: `reduck/mail.google.com/list_inbox`
- Updated: 2026-08-27 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mail.google.com/list_inbox`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mail.google.com/list_inbox
```

## Input

It takes no input.

## Output

- `rows` (array, required)
- `folder` (string | null, required)
- `total` (string | null, optional): Range/count line as rendered, e.g. '1-50 of 240'.

## FAQ

### What does "List Gmail inbox" do?

List the messages on the first page of the Gmail inbox. Requires an authenticated mail.google.com session. Returns folder, total (the range line as rendered, e.g. "1–50 of 240") and rows of sender, subject, snippet, date plus the unread / starred / hasAttachment flags. Covers only the first inbox page (up to ~50 rows as Gmail renders it); there is no pagination. Be aware that the output requires at least one row, so a genuinely empty inbox is not representable and will surface as a failure rather than an empty list.

### How do I automatically list Gmail inbox on mail.google.com?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/list_inbox, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/list_inbox

### Is there a mail.google.com API to list Gmail inbox?

You do not need one. "List Gmail inbox" drives the real mail.google.com pages in a browser, so it works whether or not mail.google.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns rows, total, folder.

### Do I need to be logged in to mail.google.com?

Yes. It acts as you on mail.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mail.google.com cookies saved by the Reduck extension.

### Does it change anything on mail.google.com, or only read data?

It only reads. It looks things up on mail.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/list_inbox, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/list_inbox

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/mail.google.com/list_inbox
