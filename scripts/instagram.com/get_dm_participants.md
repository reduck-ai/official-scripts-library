# Get Instagram DM participants

Automatically get Instagram DM participants on instagram.com. List the participants of an Instagram DM thread by thread_id (from get_inbox) — mainly useful for group DMs. Returns each participant's username, full name, profile picture and whether they are the viewer or a group admin.

- Site: instagram.com
- Address: `reduck/instagram.com/get_dm_participants`
- Updated: 2026-09-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/get_dm_participants`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_dm_participants
```

## Input

- `threadId` (string, required): Instagram DM thread id (the thread_id field from instagram.com/get_inbox).

## Output

- `count` (integer, required)
- `threadId` (string, required)
- `participants` (array, required)
- `isGroup` (boolean | null, optional)
- `threadTitle` (string | null, optional)

## FAQ

### What does "Get Instagram DM participants" do?

List the participants of an Instagram DM thread by thread_id (from get_inbox) — mainly useful for group DMs. Returns each participant's username, full name, profile picture and whether they are the viewer or a group admin.

### How do I automatically get Instagram DM participants on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_dm_participants, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_dm_participants

### Is there a instagram.com API to get Instagram DM participants?

You do not need one. "Get Instagram DM participants" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: threadId.

### What does it return?

It returns count, isGroup, threadId, threadTitle, participants.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It only reads. It looks things up on instagram.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_dm_participants, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_dm_participants

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/get_dm_participants
