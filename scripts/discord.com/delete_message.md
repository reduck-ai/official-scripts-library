# Delete Discord message

Automatically delete Discord message on discord.com. Deletes a single Discord message by id (e.g. to clean up a message you sent). Requires being logged in as the message's author or having Manage Messages in the channel.

- Site: discord.com
- Address: `reduck/discord.com/delete_message`
- Updated: 2026-09-14 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/discord.com/delete_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/discord.com/delete_message
```

## Input

- `messageId` (string, required): ID of the message to delete (from post_message's or read_messages' output).
- `channelUrl` (string, required): Full channel URL, e.g. https://discord.com/channels/<guildId>/<channelId>

## Output

- `deleted` (boolean, required)
- `messageId` (string, required)

## FAQ

### What does "Delete Discord message" do?

Deletes a single Discord message by id (e.g. to clean up a message you sent). Requires being logged in as the message's author or having Manage Messages in the channel.

### How do I automatically delete Discord message on discord.com?

Ask an AI agent connected to Reduck to run reduck/discord.com/delete_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/delete_message

### Is there a discord.com API to delete Discord message?

You do not need one. "Delete Discord message" drives the real discord.com pages in a browser, so it works whether or not discord.com offers an API for this.

### What information do I need to provide?

Required: channelUrl, messageId.

### What does it return?

It returns deleted, messageId.

### Do I need to be logged in to discord.com?

Yes. It acts as you on discord.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the discord.com cookies saved by the Reduck extension.

### Does it change anything on discord.com, or only read data?

It makes changes on discord.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/discord.com/delete_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/delete_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/discord.com/delete_message
