# Delete an Outlook.com email

Automatically delete an Outlook.com email on outlook.live.com. Delete one received Outlook.com (outlook.live.com) message by its id (from list_emails). Confirms the message is actually gone and that exactly one message was removed, rather than assuming the action worked, and then reports whether it is still recoverable: deleting from an ordinary folder files the message in Deleted Items, while deleting from Junk Email destroys it outright. When it is recoverable the id it now has in Deleted Items is returned. Drafts are not supported, because selecting a draft opens it in the composer. Deleting from Deleted Items is also refused, since that is permanent and Outlook gates it behind a confirmation dialog.

- Site: outlook.live.com
- Address: `reduck/outlook.live.com/delete_email`
- Updated: 2026-09-16 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/outlook.live.com/delete_email`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/delete_email
```

## Input

- `id` (string, required): Message id from list_emails (the row's id attribute).
- `folder` (string, optional): Folder the message lives in, named as it appears in your folder list (e.g. Inbox, Archive, Junk Email). Case and surrounding spaces do not matter. Two folders are refused rather than half-supported: Drafts, because selecting a draft opens it in the composer, and Deleted Items, because deleting there is permanent and Outlook gates it behind a confirmation dialog.

## Output

- `id` (string, required)
- `folder` (string, required)
- `deleted` (boolean, required): True only when the target row is gone AND no other row disappeared with it. Never inferred from the keypress.
- `permanent` (boolean, required): True when the message is NOT recoverable from Deleted Items. Only trust this when recoverabilityConfirmed is true — deleting from Junk Email destroys a message outright, while deleting from an ordinary folder files it in Deleted Items.
- `remaining` (number, optional): Rows still rendered in the source folder. The list is virtualised and backfills, so this is not a folder total and is not used to verify the deletion.
- `recoverableAs` (string | null, optional): The id the message now has in Deleted Items, when it was found there. Outlook gives a message a new id per folder, so the id passed in will not find it.
- `recoverabilityConfirmed` (boolean, optional): Whether the recoverability verdict was actually established by looking. False means Deleted Items could not be read conclusively (its list is virtualised), so `permanent` is a default rather than a finding and the message may well still be recoverable.

## FAQ

### What does "Delete an Outlook.com email" do?

Delete one received Outlook.com (outlook.live.com) message by its id (from list_emails). Confirms the message is actually gone and that exactly one message was removed, rather than assuming the action worked, and then reports whether it is still recoverable: deleting from an ordinary folder files the message in Deleted Items, while deleting from Junk Email destroys it outright. When it is recoverable the id it now has in Deleted Items is returned. Drafts are not supported, because selecting a draft opens it in the composer. Deleting from Deleted Items is also refused, since that is permanent and Outlook gates it behind a confirmation dialog.

### How do I automatically delete an Outlook.com email on outlook.live.com?

Ask an AI agent connected to Reduck to run reduck/outlook.live.com/delete_email, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/delete_email

### Is there a outlook.live.com API to delete an Outlook.com email?

You do not need one. "Delete an Outlook.com email" drives the real outlook.live.com pages in a browser, so it works whether or not outlook.live.com offers an API for this.

### What information do I need to provide?

Required: id. Optional: folder.

### What does it return?

It returns id, folder, deleted, permanent, remaining, recoverableAs, recoverabilityConfirmed.

### Do I need to be logged in to outlook.live.com?

Yes. It acts as you on outlook.live.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the outlook.live.com cookies saved by the Reduck extension.

### Does it change anything on outlook.live.com, or only read data?

It makes changes on outlook.live.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/outlook.live.com/delete_email, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/delete_email

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/outlook.live.com/delete_email
