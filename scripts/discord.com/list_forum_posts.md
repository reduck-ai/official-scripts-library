# List Discord forum posts

Automatically list Discord forum posts on discord.com. List the posts (threads) of a Discord forum channel, newest first, active and archived alike, optionally only those Discord's forum search matches for a text. Large forums are read in full: limit sets how many come back in one call, and next_offset, passed back as offset, reads the next ones; total_results is Discord's count of matching posts. Per post: threadId, name, url, createdAt, the author (id, username, and the name the server shows), Discord's message count, the opening message, tags (id and name), and whether it is archived, locked or pinned. Pass a post's url to discord.com/read_messages to read its replies. Reading marks nothing as read. Fails with a clear error when the channel is a text channel (use discord.com/read_messages), when the account is not in the server, or when its roles do not let it read the forum's posts. Requires being signed in.

- Site: discord.com
- Address: `reduck/discord.com/list_forum_posts`
- Updated: 2026-11-11 (v21)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/discord.com/list_forum_posts`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/discord.com/list_forum_posts
```

## Input

- `channelUrl` (string, required): Full forum channel URL, e.g. https://discord.com/channels/<guildId>/<channelId>. Get one from discord.com/list_channels.
- `limit` (integer, optional): How many posts to return, newest first. Fewer come back when the forum is shorter.
- `query` (string, optional): Only the posts Discord's forum search matches for this text. Omitted: every post.
- `offset` (integer, optional): How many posts to skip, newest first: pass next_offset of the previous answer to read the next posts.

## Output

- `count` (integer, required)
- `posts` (array, required): Newest first.
- `complete` (boolean, required): True when no post remains after these, from offset on.
- `channelId` (string, required)
- `next_offset` (integer | null, required): Pass as offset to read the next posts; null when complete.
- `total_results` (integer | null, required): Discord's count of posts that match (all posts without query).

## FAQ

### What does "List Discord forum posts" do?

List the posts (threads) of a Discord forum channel, newest first, active and archived alike, optionally only those Discord's forum search matches for a text. Large forums are read in full: limit sets how many come back in one call, and next_offset, passed back as offset, reads the next ones; total_results is Discord's count of matching posts. Per post: threadId, name, url, createdAt, the author (id, username, and the name the server shows), Discord's message count, the opening message, tags (id and name), and whether it is archived, locked or pinned. Pass a post's url to discord.com/read_messages to read its replies. Reading marks nothing as read. Fails with a clear error when the channel is a text channel (use discord.com/read_messages), when the account is not in the server, or when its roles do not let it read the forum's posts. Requires being signed in.

### How do I automatically list Discord forum posts on discord.com?

Ask an AI agent connected to Reduck to run reduck/discord.com/list_forum_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/list_forum_posts

### Is there a discord.com API to list Discord forum posts?

You do not need one. "List Discord forum posts" drives the real discord.com pages in a browser, so it works whether or not discord.com offers an API for this.

### What information do I need to provide?

Required: channelUrl. Optional: limit, query, offset.

### What does it return?

It returns count, posts, complete, channelId, next_offset, total_results.

### Do I need to be logged in to discord.com?

Yes. It acts as you on discord.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the discord.com cookies saved by the Reduck extension.

### Does it change anything on discord.com, or only read data?

It only reads. It looks things up on discord.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/discord.com/list_forum_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/list_forum_posts

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/discord.com/list_forum_posts
