# get_member_list

List the members shown in a Discord server's member sidebar for a given channel. Returns per member their userId, display name without the role badges the row also renders, and whether Discord marks them as an app. userId is null for a member on a default avatar, which carries no id to read. Discord only sends the sidebar the members near the scroll position, so a large server returns those rendered while scrolling rather than a guaranteed roster; complete says which happened, and offline members are omitted where Discord collapses them. The sidebar's role grouping is not returned, as the headings expose no stable handle.

- Site: discord.com
- Address: `reduck/discord.com/get_member_list`
- Updated: 2026-09-15 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/discord.com/get_member_list`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/discord.com/get_member_list
```

## Input

- `channelUrl` (string, required): URL of a text channel in the server, e.g. https://discord.com/channels/<guildId>/<channelId>. The member sidebar belongs to the channel, so it must be one the account can view.
- `limit` (integer, optional): How many members to return.

## Output

- `count` (integer, required)
- `members` (array, required)
- `guildId` (string | null, optional)
- `complete` (boolean, optional): True when the sidebar stopped yielding new members before limit was reached. Discord only sends the sidebar members near the scroll position, so a large server can return fewer than it holds.

## FAQ

### What does "get_member_list" do?

List the members shown in a Discord server's member sidebar for a given channel. Returns per member their userId, display name without the role badges the row also renders, and whether Discord marks them as an app. userId is null for a member on a default avatar, which carries no id to read. Discord only sends the sidebar the members near the scroll position, so a large server returns those rendered while scrolling rather than a guaranteed roster; complete says which happened, and offline members are omitted where Discord collapses them. The sidebar's role grouping is not returned, as the headings expose no stable handle.

### What information do I need to provide?

Required: channelUrl. Optional: limit.

### What does it return?

It returns count, guildId, members, complete.

### Do I need to be logged in to discord.com?

Yes. It acts as you on discord.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the discord.com cookies saved by the Reduck extension.

### Does it change anything on discord.com, or only read data?

It only reads. It looks things up on discord.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/discord.com/get_member_list, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/get_member_list

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/discord.com/get_member_list
