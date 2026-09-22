# create_channel

Create a channel in a Discord server — text, voice, announcement, stage or forum — optionally inside a category. Requires the Manage Channels permission in that server. Returns the created channel's channelId, name, type, url, parentId and the guildId, read from Discord's own creation response rather than the sidebar, plus already_present when a channel of that name and type already exists in the target category (it is reported, not duplicated — Discord itself allows duplicate channel names). Note Discord lowercases and hyphenates text/forum channel names, so the returned name may differ from the one you passed.

- Site: discord.com
- Address: `reduck/discord.com/create_channel`
- Updated: 2026-09-09 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/discord.com/create_channel`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/discord.com/create_channel
```

## Input

- `name` (string, required): Channel name. Discord lowercases it and replaces spaces with hyphens for text and forum channels; voice and stage names keep their casing.
- `guildId` (string, required): Server id, e.g. from discord.com/list_servers.
- `type` (any, optional): Channel type to create. 'forum' creates a posts-only channel (list its posts with discord.com/list_forum_posts). announcement and stage require Community to be enabled on the server.
- `categoryId` (string, optional): Optional category (parent) id to create the channel inside, e.g. from the categories array of discord.com/list_channels. Omit to create it outside any category.

## Output

- `name` (string, required)
- `type` (string, required)
- `guildId` (string, required)
- `channelId` (string, required)
- `already_present` (boolean, required)
- `url` (string | null, optional)
- `parentId` (string | null, optional)
- `typeCode` (integer | null, optional)
- `verified_on_page` (boolean, optional): Whether the new channel was confirmed present in the sidebar after creation, rather than only trusting the creation response.

## FAQ

### What does "create_channel" do?

Create a channel in a Discord server — text, voice, announcement, stage or forum — optionally inside a category. Requires the Manage Channels permission in that server. Returns the created channel's channelId, name, type, url, parentId and the guildId, read from Discord's own creation response rather than the sidebar, plus already_present when a channel of that name and type already exists in the target category (it is reported, not duplicated — Discord itself allows duplicate channel names). Note Discord lowercases and hyphenates text/forum channel names, so the returned name may differ from the one you passed.

### What information do I need to provide?

Required: guildId, name. Optional: type, categoryId.

### What does it return?

It returns url, name, type, guildId, parentId, typeCode, channelId, already_present, verified_on_page.

### Do I need to be logged in to discord.com?

Yes. It acts as you on discord.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the discord.com cookies saved by the Reduck extension.

### Does it change anything on discord.com, or only read data?

It makes changes on discord.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/discord.com/create_channel, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/create_channel

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/discord.com/create_channel
