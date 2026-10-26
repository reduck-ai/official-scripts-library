# Get Skool direct-message inbox

Automatically get Skool direct-message inbox on skool.com. List the direct-message conversations in the signed-in Skool account's inbox, in the order Skool gives them. For each conversation: the other person's display name, profile handle and profile URL, the last message's text and time, whether it is unread and how many unread messages it holds, and whether the account itself sent the last message. Messaging on Skool is per account, so this covers every community the account belongs to. Conversations have no page of their own on Skool, so each one links to the other person's profile. limit caps how many are returned; complete is false when more exist. An empty inbox returns an empty list. A signed-out browser fails with a signed-out error asking to sign in to skool.com.

- Site: skool.com
- Address: `reduck/skool.com/get_dms_inbox`
- Updated: 2026-10-22 (v14)
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

### What does "Get Skool direct-message inbox" do?

List the direct-message conversations in the signed-in Skool account's inbox, in the order Skool gives them. For each conversation: the other person's display name, profile handle and profile URL, the last message's text and time, whether it is unread and how many unread messages it holds, and whether the account itself sent the last message. Messaging on Skool is per account, so this covers every community the account belongs to. Conversations have no page of their own on Skool, so each one links to the other person's profile. limit caps how many are returned; complete is false when more exist. An empty inbox returns an empty list. A signed-out browser fails with a signed-out error asking to sign in to skool.com.

### How do I automatically get Skool direct-message inbox on skool.com?

Ask an AI agent connected to Reduck to run reduck/skool.com/get_dms_inbox, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/skool.com/get_dms_inbox

### Is there a skool.com API to get Skool direct-message inbox?

You do not need one. "Get Skool direct-message inbox" drives the real skool.com pages in a browser, so it works whether or not skool.com offers an API for this.

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
