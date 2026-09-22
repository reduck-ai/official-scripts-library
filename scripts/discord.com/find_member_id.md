# Find Discord member ID by name

Automatically find Discord member ID by name on discord.com. Resolves a Discord member's userId from their name, through a channel's mention autocomplete (@name). Useful to build a <@id> ping. Requires being logged in.

- Site: discord.com
- Address: `reduck/discord.com/find_member_id`
- Updated: 2026-09-03 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/discord.com/find_member_id`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/discord.com/find_member_id
```

## Input

- `name` (string, required): Name (or start of the name) of the member to resolve. Throws when no member matches.
- `channelUrl` (string, required): URL of a channel in the server to search, e.g. https://discord.com/channels/<guildId>/<channelId>. Must be a channel the signed-in account can type in (the lookup runs through that channel's message box).

## Output

- `userId` (string | null, required): userId of the first result (best match), or null.
- `matches` (array, required): All members offered by the autocomplete, best first.

## FAQ

### What does "Find Discord member ID by name" do?

Resolves a Discord member's userId from their name, through a channel's mention autocomplete (@name). Useful to build a <@id> ping. Requires being logged in.

### How do I automatically find Discord member ID by name on discord.com?

Ask an AI agent connected to Reduck to run reduck/discord.com/find_member_id, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/find_member_id

### Is there a discord.com API to find Discord member ID by name?

You do not need one. "Find Discord member ID by name" drives the real discord.com pages in a browser, so it works whether or not discord.com offers an API for this.

### What information do I need to provide?

Required: channelUrl, name.

### What does it return?

It returns userId, matches.

### Do I need to be logged in to discord.com?

Yes. It acts as you on discord.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the discord.com cookies saved by the Reduck extension.

### Does it change anything on discord.com, or only read data?

It only reads. It looks things up on discord.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/discord.com/find_member_id, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/find_member_id

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/discord.com/find_member_id
