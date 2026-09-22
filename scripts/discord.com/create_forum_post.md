# Create a Discord forum post

Automatically create a Discord forum post on discord.com. Create a post (thread) in a Discord forum channel, with a title and an opening message. Forum channels reject plain messages — a post is the only way to write to one, which is why discord.com/post_message cannot target a forum. Returns the new post's threadId, name, url, parentId and the opening message id, read from Discord's own creation response. Reply to an existing post with discord.com/post_message against the post's own url (a post is itself a channel), and list a forum's posts with discord.com/list_forum_posts.

- Site: discord.com
- Address: `reduck/discord.com/create_forum_post`
- Updated: 2026-08-27 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/discord.com/create_forum_post`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/discord.com/create_forum_post
```

## Input

- `title` (string, required): The post title, shown as the thread name in the forum listing. An existing post with this exact title is reported rather than duplicated.
- `content` (string, required): The opening message body of the post.
- `channelUrl` (string, required): Full forum channel URL, e.g. https://discord.com/channels/<guildId>/<channelId>. Get one from discord.com/list_channels or create one with discord.com/create_channel (type: forum).

## Output

- `url` (string, required)
- `name` (string, required)
- `threadId` (string, required)
- `already_present` (boolean, required): True when a post with this exact title already existed, in which case it is reported rather than duplicated.
- `parentId` (string | null, optional)
- `verified_on_page` (boolean, optional): Whether the post was confirmed present in the forum grid after creation.
- `response_captured` (boolean, optional): False when Discord's creation response was not observed and the post was identified from the grid instead. The post is still real; only the response was missed.

## FAQ

### What does "Create a Discord forum post" do?

Create a post (thread) in a Discord forum channel, with a title and an opening message. Forum channels reject plain messages — a post is the only way to write to one, which is why discord.com/post_message cannot target a forum. Returns the new post's threadId, name, url, parentId and the opening message id, read from Discord's own creation response. Reply to an existing post with discord.com/post_message against the post's own url (a post is itself a channel), and list a forum's posts with discord.com/list_forum_posts.

### How do I automatically create a Discord forum post on discord.com?

Ask an AI agent connected to Reduck to run reduck/discord.com/create_forum_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/create_forum_post

### Is there a discord.com API to create a Discord forum post?

You do not need one. "Create a Discord forum post" drives the real discord.com pages in a browser, so it works whether or not discord.com offers an API for this.

### What information do I need to provide?

Required: channelUrl, title, content.

### What does it return?

It returns url, name, parentId, threadId, already_present, verified_on_page, response_captured.

### Do I need to be logged in to discord.com?

Yes. It acts as you on discord.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the discord.com cookies saved by the Reduck extension.

### Does it change anything on discord.com, or only read data?

It makes changes on discord.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/discord.com/create_forum_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/create_forum_post

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/discord.com/create_forum_post
