# List Outlook.com mail folders

Automatically list Outlook.com mail folders on outlook.live.com. List the signed-in Outlook.com (outlook.live.com) account's mail folders — Inbox, Junk Email, Drafts, Sent Items, Deleted Items, Archive, Conversation History, Notes and any custom folders — from the navigation pane's folder tree. Returns each folder's name and whether it's currently selected.

- Site: outlook.live.com
- Address: `reduck/outlook.live.com/list_folders`
- Updated: 2026-09-18 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/outlook.live.com/list_folders`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/list_folders
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `folders` (array, required)

## FAQ

### What does "List Outlook.com mail folders" do?

List the signed-in Outlook.com (outlook.live.com) account's mail folders — Inbox, Junk Email, Drafts, Sent Items, Deleted Items, Archive, Conversation History, Notes and any custom folders — from the navigation pane's folder tree. Returns each folder's name and whether it's currently selected.

### How do I automatically list Outlook.com mail folders on outlook.live.com?

Ask an AI agent connected to Reduck to run reduck/outlook.live.com/list_folders, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/list_folders

### Is there a outlook.live.com API to list Outlook.com mail folders?

You do not need one. "List Outlook.com mail folders" drives the real outlook.live.com pages in a browser, so it works whether or not outlook.live.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, folders.

### Do I need to be logged in to outlook.live.com?

Yes. It acts as you on outlook.live.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the outlook.live.com cookies saved by the Reduck extension.

### Does it change anything on outlook.live.com, or only read data?

It only reads. It looks things up on outlook.live.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/outlook.live.com/list_folders, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/list_folders

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/outlook.live.com/list_folders
