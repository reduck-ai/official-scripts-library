# List Discord mentions

Automatically list Discord mentions on discord.com. Lists the recent messages that mention the signed-in Discord account, newest first, as the Inbox's Mentions tab shows them, read or not. Discord keeps mentions there for about 7 days. Filter to one server with guild_id (from discord.com/list_servers), and choose whether @everyone/@here and role mentions count. Returns up to 25 per page; pass the last message's id as before to read the next page (next_before is null on the last page). Each mention gives the message id, its channel and server (ids and names), author, time, text and link. Nothing is marked as read. Requires being signed in.

- Site: discord.com
- Address: `reduck/discord.com/list_mentions`
- Updated: 2026-11-09 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/discord.com/list_mentions`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/discord.com/list_mentions
```

## Input

- `before` (string, optional): A message id: read the mentions older than it (next_before of the previous page).
- `guild_id` (string, optional): Only mentions in this server. Get ids from discord.com/list_servers.
- `include_roles` (boolean, optional): Count mentions of a role the account has.
- `include_everyone` (boolean, optional): Count @everyone and @here.

## Output

- `count` (integer, required)
- `mentions` (array, required)
- `next_before` (string | null, required): Pass as before for the next page; null when this page is the last.

## FAQ

### What does "List Discord mentions" do?

Lists the recent messages that mention the signed-in Discord account, newest first, as the Inbox's Mentions tab shows them, read or not. Discord keeps mentions there for about 7 days. Filter to one server with guild_id (from discord.com/list_servers), and choose whether @everyone/@here and role mentions count. Returns up to 25 per page; pass the last message's id as before to read the next page (next_before is null on the last page). Each mention gives the message id, its channel and server (ids and names), author, time, text and link. Nothing is marked as read. Requires being signed in.

### How do I automatically list Discord mentions on discord.com?

Ask an AI agent connected to Reduck to run reduck/discord.com/list_mentions, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/list_mentions

### Is there a discord.com API to list Discord mentions?

You do not need one. "List Discord mentions" drives the real discord.com pages in a browser, so it works whether or not discord.com offers an API for this.

### What information do I need to provide?

Optional: before, guild_id, include_roles, include_everyone.

### What does it return?

It returns count, mentions, next_before.

### Do I need to be logged in to discord.com?

Yes. It acts as you on discord.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the discord.com cookies saved by the Reduck extension.

### Does it change anything on discord.com, or only read data?

It only reads. It looks things up on discord.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/discord.com/list_mentions, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/list_mentions

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/discord.com/list_mentions
