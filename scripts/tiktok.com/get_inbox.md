# Get TikTok direct message inbox

Automatically get TikTok direct message inbox on tiktok.com. List the signed-in account's direct message conversations, newest activity first: who each one is with, the last message preview as the inbox shows it, and the timestamp label. Handles and nicknames are resolved for every participant, so a conversation can be read afterwards with the get-conversation script. This is the private messages list, not the activity feed of likes and follows — use the notifications script for those.

- Site: tiktok.com
- Address: `reduck/tiktok.com/get_inbox`
- Updated: 2026-09-03 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/get_inbox`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_inbox
```

## Input

- `count` (integer, optional): Target number of conversations to collect; the inbox list is scrolled until this many are gathered or it ends.

## Output

- `hasMore` (boolean, required): True when the inbox still had conversations beyond the ones returned.
- `account_used` (string, required): Handle whose inbox was read, from the signed-in session.
- `conversations` (array, required)

## FAQ

### What does "Get TikTok direct message inbox" do?

List the signed-in account's direct message conversations, newest activity first: who each one is with, the last message preview as the inbox shows it, and the timestamp label. Handles and nicknames are resolved for every participant, so a conversation can be read afterwards with the get-conversation script. This is the private messages list, not the activity feed of likes and follows — use the notifications script for those.

### How do I automatically get TikTok direct message inbox on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_inbox, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_inbox

### Is there a tiktok.com API to get TikTok direct message inbox?

You do not need one. "Get TikTok direct message inbox" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Optional: count.

### What does it return?

It returns hasMore, account_used, conversations.

### Do I need to be logged in to tiktok.com?

Yes. It acts as you on tiktok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the tiktok.com cookies saved by the Reduck extension.

### Does it change anything on tiktok.com, or only read data?

It only reads. It looks things up on tiktok.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_inbox, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_inbox

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/get_inbox
