# get_dms_inbox

List the direct-message conversations in the signed-in Skool account's inbox, newest activity first. Returns per conversation the other participant's display name, profile handle and profile URL, the last message's text and time, whether it is unread and how many unread it holds, and whether the last message was sent by the account itself. Skool scopes messaging per account rather than per community, so this covers every community the account belongs to. Note: Skool's DM surface is a flyout with no addressable per-conversation URL (/chat, /chats and ?c= all redirect to the group page), so conversations expose the participant's profileUrl rather than a thread link. Throws if the account is signed out, rather than reporting an empty inbox.

- Site: skool.com
- Address: `reduck/skool.com/get_dms_inbox`
- Updated: 2026-09-17 (v12)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/skool.com/get_dms_inbox`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/skool.com/get_dms_inbox
```

## Input

- `limit` (integer, optional): How many conversations to return, newest activity first.

## Output

- `count` (integer, required): Number of conversations returned.
- `complete` (boolean, required): True when the whole inbox was returned (not truncated by limit).
- `conversations` (array, required)

## FAQ

### What does "get_dms_inbox" do?

List the direct-message conversations in the signed-in Skool account's inbox, newest activity first. Returns per conversation the other participant's display name, profile handle and profile URL, the last message's text and time, whether it is unread and how many unread it holds, and whether the last message was sent by the account itself. Skool scopes messaging per account rather than per community, so this covers every community the account belongs to. Note: Skool's DM surface is a flyout with no addressable per-conversation URL (/chat, /chats and ?c= all redirect to the group page), so conversations expose the participant's profileUrl rather than a thread link. Throws if the account is signed out, rather than reporting an empty inbox.

### What information do I need to provide?

Optional: limit.

### What does it return?

It returns count, complete, conversations.

### Do I need to be logged in to skool.com?

Yes. It acts as you on skool.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the skool.com cookies saved by the Reduck extension.

### Does it change anything on skool.com, or only read data?

It only reads. It looks things up on skool.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/skool.com/get_dms_inbox, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/skool.com/get_dms_inbox

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/skool.com/get_dms_inbox
