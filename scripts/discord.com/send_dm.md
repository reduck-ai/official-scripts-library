# Send Discord DM

Automatically send Discord DM on discord.com. Send a direct message to a Discord user, addressed by their username. Opens (or reuses) the one-to-one DM conversation and posts the message there. Returns sent, the created message's messageId, the DM channelId, timestamp, and the content as Discord stored it, plus the recipient's resolved handle so the message is provably not sent to a near-name match. This is a write and the recipient is notified: confirm the exact recipient and text with the user before running, and note that approval for one message does not carry over to another.

- Site: discord.com
- Address: `reduck/discord.com/send_dm`
- Updated: 2026-09-16 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/discord.com/send_dm`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/discord.com/send_dm
```

## Input

- `userId` (string, required): The recipient's Discord user id, e.g. from discord.com/find_member_id or the author.id of discord.com/search_messages.
- `message` (string, required): The message text. Discord's own limit is 2000 characters.
- `expectedUsername` (string, required): The recipient's username, asserted against the handle on their profile before the message is typed. A mismatch aborts without sending, so a stale or wrong id cannot message the wrong person.

## Output

- `sent` (boolean, required)
- `channelId` (string, required): The one-to-one DM channel the message went to.
- `recipient` (string, required): The handle read from the recipient's own profile, not echoed from the input.
- `content` (string | null, optional): The content as Discord stored it.
- `messageId` (string | null, optional)
- `timestamp` (string | null, optional)

## FAQ

### What does "Send Discord DM" do?

Send a direct message to a Discord user, addressed by their username. Opens (or reuses) the one-to-one DM conversation and posts the message there. Returns sent, the created message's messageId, the DM channelId, timestamp, and the content as Discord stored it, plus the recipient's resolved handle so the message is provably not sent to a near-name match. This is a write and the recipient is notified: confirm the exact recipient and text with the user before running, and note that approval for one message does not carry over to another.

### How do I automatically send Discord DM on discord.com?

Ask an AI agent connected to Reduck to run reduck/discord.com/send_dm, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/send_dm

### Is there a discord.com API to send Discord DM?

You do not need one. "Send Discord DM" drives the real discord.com pages in a browser, so it works whether or not discord.com offers an API for this.

### What information do I need to provide?

Required: userId, expectedUsername, message.

### What does it return?

It returns sent, content, channelId, messageId, recipient, timestamp.

### Do I need to be logged in to discord.com?

Yes. It acts as you on discord.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the discord.com cookies saved by the Reduck extension.

### Does it change anything on discord.com, or only read data?

It makes changes on discord.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/discord.com/send_dm, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/send_dm

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/discord.com/send_dm
