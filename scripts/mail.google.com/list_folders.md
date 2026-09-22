# List Gmail labels / folders

Automatically list Gmail labels / folders on mail.google.com. List the Gmail labels and system folders visible to the account, with their unread counts where Gmail shows one. Distinguishes system folders (Inbox, Sent, Drafts, Spam, Bin...) from user-created labels.

- Site: mail.google.com
- Address: `reduck/mail.google.com/list_folders`
- Updated: 2026-08-24 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mail.google.com/list_folders`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mail.google.com/list_folders
```

## Input

- `account` (string, optional): Google account email to act as (authuser=). Without it Gmail picks u/0, which is nondeterministic in a multi-account browser jar.

## Output

- `count` (integer, required)
- `folders` (array, required)

## FAQ

### What does "List Gmail labels / folders" do?

List the Gmail labels and system folders visible to the account, with their unread counts where Gmail shows one. Distinguishes system folders (Inbox, Sent, Drafts, Spam, Bin...) from user-created labels.

### How do I automatically list Gmail labels / folders on mail.google.com?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/list_folders, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/list_folders

### Is there a mail.google.com API to list Gmail labels / folders?

You do not need one. "List Gmail labels / folders" drives the real mail.google.com pages in a browser, so it works whether or not mail.google.com offers an API for this.

### What information do I need to provide?

Optional: account.

### What does it return?

It returns count, folders.

### Do I need to be logged in to mail.google.com?

Yes. It acts as you on mail.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mail.google.com cookies saved by the Reduck extension.

### Does it change anything on mail.google.com, or only read data?

It only reads. It looks things up on mail.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/list_folders, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/list_folders

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/mail.google.com/list_folders
