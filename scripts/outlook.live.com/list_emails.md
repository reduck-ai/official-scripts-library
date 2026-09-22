# List Outlook.com emails in a folder

Automatically list Outlook.com emails in a folder on outlook.live.com. List messages in an Outlook.com (outlook.live.com) mail folder (default Inbox). Returns each message's id (the join key for get_email), sender display name, subject, date label as shown in the list, and preview snippet, in the order the list shows them.

- Site: outlook.live.com
- Address: `reduck/outlook.live.com/list_emails`
- Updated: 2026-09-21 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/outlook.live.com/list_emails`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/list_emails
```

## Input

- `folder` (string, optional): Folder name as shown in the folder list (e.g. Inbox, Sent Items, Drafts, Junk Email, Deleted Items, Archive)

## Output

- `count` (integer, required)
- `emails` (array, required)
- `folder` (string, required)

## FAQ

### What does "List Outlook.com emails in a folder" do?

List messages in an Outlook.com (outlook.live.com) mail folder (default Inbox). Returns each message's id (the join key for get_email), sender display name, subject, date label as shown in the list, and preview snippet, in the order the list shows them.

### How do I automatically list Outlook.com emails in a folder on outlook.live.com?

Ask an AI agent connected to Reduck to run reduck/outlook.live.com/list_emails, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/list_emails

### Is there a outlook.live.com API to list Outlook.com emails in a folder?

You do not need one. "List Outlook.com emails in a folder" drives the real outlook.live.com pages in a browser, so it works whether or not outlook.live.com offers an API for this.

### What information do I need to provide?

Optional: folder.

### What does it return?

It returns count, emails, folder.

### Do I need to be logged in to outlook.live.com?

Yes. It acts as you on outlook.live.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the outlook.live.com cookies saved by the Reduck extension.

### Does it change anything on outlook.live.com, or only read data?

It only reads. It looks things up on outlook.live.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/outlook.live.com/list_emails, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/list_emails

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/outlook.live.com/list_emails
