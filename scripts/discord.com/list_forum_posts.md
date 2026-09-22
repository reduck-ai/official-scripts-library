# List Discord forum posts

Automatically list Discord forum posts on discord.com. List the posts (threads) in a Discord forum channel, newest first. Use this instead of read_messages, which forum channels don't support; pass a returned post's url to read_messages to read its replies. Returns per post: threadId, name, url, createdAt, authorName, messageCount (Discord's reply count, excluding the opening post), openingMessage and tagNames. Does not return user ids, tag ids, or archived/locked/pinned state.

- Site: discord.com
- Address: `reduck/discord.com/list_forum_posts`
- Updated: 2026-09-03 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/discord.com/list_forum_posts`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/discord.com/list_forum_posts
```

## Input

- `channelUrl` (string, required): Full forum channel URL, e.g. https://discord.com/channels/<guildId>/<channelId>. Get one from discord.com/list_channels.
- `limit` (integer, optional): How many posts to return, newest first. Fewer come back when the forum is shorter.

## Output

- `count` (integer, required)
- `posts` (array, required)
- `channelId` (string, required)
- `complete` (boolean, optional): True when the grid stopped yielding new cards before limit was reached, so count is every post the forum listed.

## FAQ

### What does "List Discord forum posts" do?

List the posts (threads) in a Discord forum channel, newest first. Use this instead of read_messages, which forum channels don't support; pass a returned post's url to read_messages to read its replies. Returns per post: threadId, name, url, createdAt, authorName, messageCount (Discord's reply count, excluding the opening post), openingMessage and tagNames. Does not return user ids, tag ids, or archived/locked/pinned state.

### How do I automatically list Discord forum posts on discord.com?

Ask an AI agent connected to Reduck to run reduck/discord.com/list_forum_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/list_forum_posts

### Is there a discord.com API to list Discord forum posts?

You do not need one. "List Discord forum posts" drives the real discord.com pages in a browser, so it works whether or not discord.com offers an API for this.

### What information do I need to provide?

Required: channelUrl. Optional: limit.

### What does it return?

It returns count, posts, complete, channelId.

### Do I need to be logged in to discord.com?

Yes. It acts as you on discord.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the discord.com cookies saved by the Reduck extension.

### Does it change anything on discord.com, or only read data?

It only reads. It looks things up on discord.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/discord.com/list_forum_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/list_forum_posts

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/discord.com/list_forum_posts
