# Move an Outlook.com email to a folder

Automatically move an Outlook.com email to a folder on outlook.live.com. Move one Outlook.com (outlook.live.com) message to another folder by its id (from list_emails). Any folder in your folder list can be the destination, named exactly as it appears there. The move is confirmed on both sides — the message must have left the source and arrived in the destination — and because Outlook gives a message a new id in its new folder, that new id is returned for any follow-up call. Taking a message out of Junk Email is confirmed automatically without accepting Outlook's offer to stop future mail from that sender being treated as junk. Drafts are not supported.

- Site: outlook.live.com
- Address: `reduck/outlook.live.com/move_email`
- Updated: 2026-09-16 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/outlook.live.com/move_email`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/move_email
```

## Input

- `id` (string, required): Message id from list_emails (the row's id attribute).
- `toFolder` (string, required): Destination folder, named as it appears in your folder list (e.g. Archive, Deleted Items).
- `folder` (string, optional): Folder the message is currently in, as shown in your folder list.

## Output

- `id` (string, required): The message id passed in, which identified it in the source folder.
- `moved` (boolean, required): True only when the message is confirmed absent from the source AND present in the destination. Never inferred from the click.
- `folder` (string, required)
- `toFolder` (string, required)
- `newId` (string | null, optional): The id the message carries in the destination folder. Outlook reassigns it on a move, so use this for any follow-up call — the id you passed in no longer resolves.
- `leftSource` (boolean, optional): Whether the message left the source folder.
- `conversationId` (string | null, optional): Conversation id, which is the same in every folder and is what the move is verified against.
- `confirmationDialog` (boolean, optional): Whether Outlook asked for confirmation before moving, which it does when taking a message out of Junk Email. Its offer to stop future mail from that sender reaching Junk is always declined, so the move changes nothing beyond this one message.
- `arrivedInDestination` (boolean, optional): Whether it was then found in the destination folder.

## FAQ

### What does "Move an Outlook.com email to a folder" do?

Move one Outlook.com (outlook.live.com) message to another folder by its id (from list_emails). Any folder in your folder list can be the destination, named exactly as it appears there. The move is confirmed on both sides — the message must have left the source and arrived in the destination — and because Outlook gives a message a new id in its new folder, that new id is returned for any follow-up call. Taking a message out of Junk Email is confirmed automatically without accepting Outlook's offer to stop future mail from that sender being treated as junk. Drafts are not supported.

### How do I automatically move an Outlook.com email to a folder on outlook.live.com?

Ask an AI agent connected to Reduck to run reduck/outlook.live.com/move_email, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/move_email

### Is there a outlook.live.com API to move an Outlook.com email to a folder?

You do not need one. "Move an Outlook.com email to a folder" drives the real outlook.live.com pages in a browser, so it works whether or not outlook.live.com offers an API for this.

### What information do I need to provide?

Required: id, toFolder. Optional: folder.

### What does it return?

It returns id, moved, newId, folder, toFolder, leftSource, conversationId, confirmationDialog, arrivedInDestination.

### Do I need to be logged in to outlook.live.com?

Yes. It acts as you on outlook.live.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the outlook.live.com cookies saved by the Reduck extension.

### Does it change anything on outlook.live.com, or only read data?

It makes changes on outlook.live.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/outlook.live.com/move_email, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/move_email

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/outlook.live.com/move_email
