# Edit Discord message

Automatically edit Discord message on discord.com. Edit the text of one of your own Discord messages, addressed by its url. Discord marks an edited message with an "(edited)" tag visible to everyone. Returns the message's id, channel id, the new content as Discord stored it, and the edit timestamp. Only your own messages can be edited — Discord's UI offers no edit control on anyone else's.

- Site: discord.com
- Address: `reduck/discord.com/edit_message`
- Updated: 2026-09-08 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/discord.com/edit_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/discord.com/edit_message
```

## Input

- `content` (string, required): The full replacement text. This replaces the message entirely, it does not append.
- `messageUrl` (string, required): Full url of your own message, e.g. https://discord.com/channels/<guildId>/<channelId>/<messageId>. discord.com/read_messages or discord.com/search_messages return the ids to build one.

## Output

- `edited` (boolean, required)
- `content` (string, required)
- `channelId` (string, required)
- `messageId` (string, required)
- `previousContent` (string | null, required)
- `editedTimestamp` (string | null, optional)

## FAQ

### What does "Edit Discord message" do?

Edit the text of one of your own Discord messages, addressed by its url. Discord marks an edited message with an "(edited)" tag visible to everyone. Returns the message's id, channel id, the new content as Discord stored it, and the edit timestamp. Only your own messages can be edited — Discord's UI offers no edit control on anyone else's.

### How do I automatically edit Discord message on discord.com?

Ask an AI agent connected to Reduck to run reduck/discord.com/edit_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/edit_message

### Is there a discord.com API to edit Discord message?

You do not need one. "Edit Discord message" drives the real discord.com pages in a browser, so it works whether or not discord.com offers an API for this.

### What information do I need to provide?

Required: messageUrl, content.

### What does it return?

It returns edited, content, channelId, messageId, editedTimestamp, previousContent.

### Do I need to be logged in to discord.com?

Yes. It acts as you on discord.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the discord.com cookies saved by the Reduck extension.

### Does it change anything on discord.com, or only read data?

It makes changes on discord.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/discord.com/edit_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/edit_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/discord.com/edit_message
