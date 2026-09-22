# Read an Outlook.com email

Automatically read an Outlook.com email on outlook.live.com. Read one Outlook.com (outlook.live.com) message's details by its id (as returned by list_emails): subject, sender, recipient, date shown on the message, and body text. Opens the message in the current folder's reading pane.

- Site: outlook.live.com
- Address: `reduck/outlook.live.com/get_email`
- Updated: 2026-09-21 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/outlook.live.com/get_email`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/get_email
```

## Input

- `id` (string, required): Message id from list_emails (the row's id attribute)
- `folder` (string, optional): Folder the message lives in, as shown in the folder list

## Output

- `id` (string, required)
- `to` (string, required)
- `body` (string, required)
- `date` (string, required)
- `sender` (string, required)
- `subject` (string, required)

## FAQ

### What does "Read an Outlook.com email" do?

Read one Outlook.com (outlook.live.com) message's details by its id (as returned by list_emails): subject, sender, recipient, date shown on the message, and body text. Opens the message in the current folder's reading pane.

### How do I automatically read an Outlook.com email on outlook.live.com?

Ask an AI agent connected to Reduck to run reduck/outlook.live.com/get_email, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/get_email

### Is there a outlook.live.com API to read an Outlook.com email?

You do not need one. "Read an Outlook.com email" drives the real outlook.live.com pages in a browser, so it works whether or not outlook.live.com offers an API for this.

### What information do I need to provide?

Required: id. Optional: folder.

### What does it return?

It returns id, to, body, date, sender, subject.

### Do I need to be logged in to outlook.live.com?

Yes. It acts as you on outlook.live.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the outlook.live.com cookies saved by the Reduck extension.

### Does it change anything on outlook.live.com, or only read data?

It only reads. It looks things up on outlook.live.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/outlook.live.com/get_email, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/get_email

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/outlook.live.com/get_email
