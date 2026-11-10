# List unread Discord messages

Automatically list unread Discord messages on discord.com. Lists everything the signed-in Discord account has not read yet, as the Inbox's Unreads tab shows it: direct messages, group DMs, server channels, threads and forum posts, in the Inbox's order. Each conversation comes with its server and category, its url, isDm, the mention count, and its unread messages (id, author, time, text), plus the post title for forum posts. Nothing is marked as read. max_channels caps how many conversations are read (default 25); complete is false when more were left. Within one conversation the Inbox loads about the first 15 unread messages; moreMessages says when there are more, which discord.com/read_messages can read. Requires being signed in.

- Site: discord.com
- Address: `reduck/discord.com/list_unreads`
- Updated: 2026-11-09 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/discord.com/list_unreads`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/discord.com/list_unreads
```

## Input

- `max_channels` (integer, optional): Read at most this many conversations.

## Output

- `count` (integer, required)
- `complete` (boolean, required): false when max_channels stopped the read before the end of the Unreads tab.
- `conversations` (array, required)

## FAQ

### What does "List unread Discord messages" do?

Lists everything the signed-in Discord account has not read yet, as the Inbox's Unreads tab shows it: direct messages, group DMs, server channels, threads and forum posts, in the Inbox's order. Each conversation comes with its server and category, its url, isDm, the mention count, and its unread messages (id, author, time, text), plus the post title for forum posts. Nothing is marked as read. max_channels caps how many conversations are read (default 25); complete is false when more were left. Within one conversation the Inbox loads about the first 15 unread messages; moreMessages says when there are more, which discord.com/read_messages can read. Requires being signed in.

### How do I automatically list unread Discord messages on discord.com?

Ask an AI agent connected to Reduck to run reduck/discord.com/list_unreads, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/list_unreads

### Is there a discord.com API to list unread Discord messages?

You do not need one. "List unread Discord messages" drives the real discord.com pages in a browser, so it works whether or not discord.com offers an API for this.

### What information do I need to provide?

Optional: max_channels.

### What does it return?

It returns count, complete, conversations.

### Do I need to be logged in to discord.com?

Yes. It acts as you on discord.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the discord.com cookies saved by the Reduck extension.

### Does it change anything on discord.com, or only read data?

It only reads. It looks things up on discord.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/discord.com/list_unreads, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/list_unreads

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/discord.com/list_unreads
