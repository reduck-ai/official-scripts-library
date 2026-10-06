# Post a Discord message

Automatically post a Discord message on discord.com. Posts a text message, optionally with a file attached, in a Discord channel addressed by its URL. Requires being logged in to Discord. Returns `sent` plus the created message's messageId, channelId, timestamp and content as Discord stored it. The message is visible to everyone who can see the channel. Empty messages and messages over 2000 characters are refused with a clear reason. Use dry_run to check a channel and message without posting.

- Site: discord.com
- Address: `reduck/discord.com/post_message`
- Updated: 2026-10-05 (v19)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/discord.com/post_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/discord.com/post_message
```

## Input

- `channelUrl` (string, required): Full channel URL, e.g. https://discord.com/channels/<guildId>/<channelId>
- `dry_run` (boolean, optional): When true, the message and any attachment are prepared in the channel but not sent. Nothing is posted: sent comes back false, messageId is null and dry_run is true. Use it to check that a channel, message and attachment are accepted without posting a real, visible message.
- `message` (string, optional): Text of the message. Optional when a file is attached, in which case it becomes the message's caption. Up to 2000 characters.
- `filename` (string, optional): Name the file is posted under, e.g. report.csv. Required whenever fileBase64 is given. Not used with the `attachment` file input, which posts the file under the input's own name.
- `mimeType` (string, optional): Optional content type for the attachment, e.g. text/csv. Guessed from the filename extension when omitted.
- `attachment` (string, optional): A file to attach. Preferred over fileBase64 for larger files, as it is not limited to roughly 380 KB. The file is posted under the name of this input, so use fileBase64 + filename instead when the posted filename matters.
- `fileBase64` (string, optional): Optional file to attach, as base64 bytes, as an alternative to the `attachment` file input. Sent as one message together with the text. Limited to roughly 380 KB of base64, well under Discord's own upload limit. Use this when you need to control the posted filename.

## Output

- `sent` (boolean, required): False on a dry run, where nothing was posted.
- `content` (string | null, optional): Content as stored by Discord. Null on a dry run.
- `dry_run` (boolean, optional): True when this run prepared the message without sending it.
- `channelId` (string | null, optional)
- `messageId` (string | null, optional): ID of the created message. Null on a dry run.
- `timestamp` (string | null, optional)
- `attachment` (object | null, optional): The file Discord stored — null when no file was sent, and null on a dry run.

## FAQ

### What does "Post a Discord message" do?

Posts a text message, optionally with a file attached, in a Discord channel addressed by its URL. Requires being logged in to Discord. Returns `sent` plus the created message's messageId, channelId, timestamp and content as Discord stored it. The message is visible to everyone who can see the channel. Empty messages and messages over 2000 characters are refused with a clear reason. Use dry_run to check a channel and message without posting.

### How do I automatically post a Discord message on discord.com?

Ask an AI agent connected to Reduck to run reduck/discord.com/post_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/post_message

### Is there a discord.com API to post a Discord message?

You do not need one. "Post a Discord message" drives the real discord.com pages in a browser, so it works whether or not discord.com offers an API for this.

### What information do I need to provide?

Required: channelUrl. Optional: dry_run, message, filename, mimeType, attachment, fileBase64.

### What does it return?

It returns sent, content, dry_run, channelId, messageId, timestamp, attachment.

### Do I need to be logged in to discord.com?

Yes. It acts as you on discord.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the discord.com cookies saved by the Reduck extension.

### Does it change anything on discord.com, or only read data?

It makes changes on discord.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/discord.com/post_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/post_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/discord.com/post_message
