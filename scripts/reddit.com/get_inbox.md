# Get Reddit chat inbox

Automatically get Reddit chat inbox on reddit.com. List the conversations in your Reddit chat inbox (DMs), newest activity first: room id + url, name, chat type, your membership (invite = a chat request you have not accepted), unread count, the other members, and the last message with its direction and real timestamp. Returns the whole inbox, not only what's currently visible on screen. Threads are a separate surface and are not listed. Runs only via the browser extension, not the hosted cloud browser.

- Site: reddit.com
- Address: `reduck/reddit.com/get_inbox`
- Updated: 2026-09-03 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/reddit.com/get_inbox`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_inbox
```

## Input

- `limit` (integer, optional): Maximum number of conversations to return, newest activity first. Omit for every conversation the chat client holds.

## Output

- `me` (string, required): The signed-in account as chat identifies it, e.g. "@t2_29fgxvhi79:reddit.com" — the id `sent_by_me` compares senders against. Chat speaks account ids, not usernames; reddit.com/whoami names the account.
- `count` (number, required): How many conversations are returned (after `limit`).
- `conversations` (array, required)

## FAQ

### What does "Get Reddit chat inbox" do?

List the conversations in your Reddit chat inbox (DMs), newest activity first: room id + url, name, chat type, your membership (invite = a chat request you have not accepted), unread count, the other members, and the last message with its direction and real timestamp. Returns the whole inbox, not only what's currently visible on screen. Threads are a separate surface and are not listed. Runs only via the browser extension, not the hosted cloud browser.

### How do I automatically get Reddit chat inbox on reddit.com?

Ask an AI agent connected to Reduck to run reduck/reddit.com/get_inbox, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_inbox

### Is there a reddit.com API to get Reddit chat inbox?

You do not need one. "Get Reddit chat inbox" drives the real reddit.com pages in a browser, so it works whether or not reddit.com offers an API for this.

### What information do I need to provide?

Optional: limit.

### What does it return?

It returns me, count, conversations.

### Do I need to be logged in to reddit.com?

Yes. It acts as you on reddit.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the reddit.com cookies saved by the Reduck extension.

### Does it change anything on reddit.com, or only read data?

Unknown: its author has not declared whether it changes anything on reddit.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/reddit.com/get_inbox, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_inbox

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/reddit.com/get_inbox
