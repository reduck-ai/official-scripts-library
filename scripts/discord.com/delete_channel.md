# delete_channel

Delete a Discord channel by its id — text, voice, announcement, stage or forum. Requires the Manage Channels permission in that server. This cannot be undone: Discord removes the channel together with all of its message history, as its own confirmation dialog warns. Before confirming, the script checks that Discord's confirmation dialog names the very channel that was asked for, so a mis-targeted context menu can never remove the wrong channel, and it refuses outright when the id is a category rather than a channel. Success is taken from Discord's own deletion response, not from the sidebar. Pass expectedName to have the channel's name asserted as well.

- Site: discord.com
- Address: `reduck/discord.com/delete_channel`
- Updated: 2026-09-09 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/discord.com/delete_channel`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/discord.com/delete_channel
```

## Input

- `guildId` (string, required): Server id the channel belongs to, e.g. from discord.com/list_servers.
- `channelId` (string, required): Id of the channel to delete, e.g. from discord.com/list_channels or create_channel's channelId. Must be a channel, not a category — a category id is refused.
- `expectedName` (string, optional): Optional safety check: the channel's name as it appears in the sidebar (from discord.com/list_channels). When given, the script refuses to delete unless the channel at channelId carries exactly this name. Regardless of this argument, the script always verifies that Discord's own confirmation dialog names the channel it resolved.

## Output

- `name` (string, required): The channel's name as read from the sidebar before deletion, so the caller has a receipt of what was actually removed.
- `deleted` (boolean, required): True only when Discord's own DELETE request returned a success status.
- `guildId` (string, required)
- `channelId` (string, required)
- `verified_gone` (boolean, required): Whether the channel row was confirmed to have disappeared from the sidebar afterwards. A second check, never the assertion — `deleted` is what Discord's API said.

## FAQ

### What does "delete_channel" do?

Delete a Discord channel by its id — text, voice, announcement, stage or forum. Requires the Manage Channels permission in that server. This cannot be undone: Discord removes the channel together with all of its message history, as its own confirmation dialog warns. Before confirming, the script checks that Discord's confirmation dialog names the very channel that was asked for, so a mis-targeted context menu can never remove the wrong channel, and it refuses outright when the id is a category rather than a channel. Success is taken from Discord's own deletion response, not from the sidebar. Pass expectedName to have the channel's name asserted as well.

### What information do I need to provide?

Required: guildId, channelId. Optional: expectedName.

### What does it return?

It returns name, deleted, guildId, channelId, verified_gone.

### Do I need to be logged in to discord.com?

Yes. It acts as you on discord.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the discord.com cookies saved by the Reduck extension.

### Does it change anything on discord.com, or only read data?

It makes changes on discord.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/discord.com/delete_channel, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/delete_channel

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/discord.com/delete_channel
