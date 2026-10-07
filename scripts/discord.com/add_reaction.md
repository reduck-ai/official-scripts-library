# add_reaction

React to a Discord message with a unicode emoji, or remove your own reaction with remove:true. Takes the message's url, as copied from Discord or built from discord.com/read_messages. Returns the emoji, the message and channel ids, whether your reaction was already there, and the reaction count afterwards. Reactions are visible to everyone who can see the channel. Supports a set of common emoji (thumbs up/down, heart, fire, eyes, check mark and similar), not every emoji and not custom server emoji. Does not work on a forum post's opening message; react to a reply in the post instead.

- Site: discord.com
- Address: `reduck/discord.com/add_reaction`
- Updated: 2026-10-06 (v30)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/discord.com/add_reaction`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/discord.com/add_reaction
```

## Input

- `emoji` (string, required): A single unicode emoji, e.g. a thumbs up. Limited to a set of common emoji (thumbs up/down, heart, laughing, fire, 100, eyes, check mark, clap, party popper, thinking, and a few more); an emoji outside that set is refused with a clear reason. Custom server emoji are not supported.
- `messageUrl` (string, required): Full message url, e.g. https://discord.com/channels/<guildId>/<channelId>/<messageId>. discord.com/read_messages returns the ids to build one. A forum or thread post's own opening message (where the channelId and messageId are equal) is not supported and is refused; react to a reply inside the post instead.
- `remove` (boolean, optional): Leave false (the default) to add your reaction. Set true to take your own reaction off; other people's reactions are never touched.

## Output

- `emoji` (string, required)
- `reacted` (boolean, required): Whether your reaction is on the message after this run.
- `channelId` (string, required)
- `messageId` (string, required)
- `already_present` (boolean, required): True when the message was already in the requested state, so nothing was written.
- `count` (integer | null, optional): How many people have reacted with this emoji afterwards; null once no one has.
- `request_seen` (boolean, optional): Whether Discord confirmed the change.

## FAQ

### What does "add_reaction" do?

React to a Discord message with a unicode emoji, or remove your own reaction with remove:true. Takes the message's url, as copied from Discord or built from discord.com/read_messages. Returns the emoji, the message and channel ids, whether your reaction was already there, and the reaction count afterwards. Reactions are visible to everyone who can see the channel. Supports a set of common emoji (thumbs up/down, heart, fire, eyes, check mark and similar), not every emoji and not custom server emoji. Does not work on a forum post's opening message; react to a reply in the post instead.

### What information do I need to provide?

Required: messageUrl, emoji. Optional: remove.

### What does it return?

It returns count, emoji, reacted, channelId, messageId, request_seen, already_present.

### Do I need to be logged in to discord.com?

Yes. It acts as you on discord.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the discord.com cookies saved by the Reduck extension.

### Does it change anything on discord.com, or only read data?

It makes changes on discord.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/discord.com/add_reaction, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/add_reaction

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/discord.com/add_reaction
