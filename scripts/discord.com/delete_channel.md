# delete_channel

Delete a Discord channel by its id — text, voice, announcement, stage or forum. Requires the Manage Channels permission in that server. This cannot be undone: the channel and all of its message history are removed. Category ids are refused. The script makes sure it is deleting exactly the channel you asked for; pass expectedName to also require that the channel has that name. Returns whether Discord confirmed the deletion and the name of the channel removed.

- Site: discord.com
- Address: `reduck/discord.com/delete_channel`
- Updated: 2026-10-05 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/discord.com/delete_channel`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/discord.com/delete_channel
```

## Input

- `guildId` (string, required): Server id the channel belongs to, e.g. from discord.com/list_servers.
- `channelId` (string, required): Id of the channel to delete, e.g. from discord.com/list_channels or create_channel's channelId. Must be a channel, not a category — a category id is refused.
- `expectedName` (string, optional): Optional safety check: the channel's name as shown in Discord (from discord.com/list_channels). When given, nothing is deleted unless the channel at channelId has exactly this name.

## Output

- `name` (string, required): The name of the channel that was deleted, as a receipt of what was removed.
- `deleted` (boolean, required): True only when Discord confirmed the deletion.
- `guildId` (string, required)
- `channelId` (string, required)
- `verified_gone` (boolean, required): Whether the channel was also confirmed gone from the server's channel list afterwards.

## FAQ

### What does "delete_channel" do?

Delete a Discord channel by its id — text, voice, announcement, stage or forum. Requires the Manage Channels permission in that server. This cannot be undone: the channel and all of its message history are removed. Category ids are refused. The script makes sure it is deleting exactly the channel you asked for; pass expectedName to also require that the channel has that name. Returns whether Discord confirmed the deletion and the name of the channel removed.

### What information do I need to provide?

Required: guildId, channelId. Optional: expectedName.

### What does it return?

It returns name, deleted, guildId, channelId, verified_gone.

### Do I need to be logged in to discord.com?

Yes. It acts as you on discord.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the discord.com cookies saved by the Reduck extension.

### Does it change anything on discord.com, or only read data?

It makes changes on discord.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/discord.com/delete_channel, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/delete_channel

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/discord.com/delete_channel
