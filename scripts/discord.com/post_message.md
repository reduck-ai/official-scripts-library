# Post a Discord message

Automatically post a Discord message on discord.com. Posts a text message in a Discord channel, addressed by channel URL. Requires being logged in to Discord. Returns `sent` plus the created message's messageId, channelId, timestamp and content as Discord stored it. This is a write: the message appears in the channel and is visible to everyone who can see it. Discord's own message limits are checked before anything is sent, so a message that is empty or whitespace-only, or longer than 2000 characters, is refused straight away with a clear reason.

- Site: discord.com
- Address: `reduck/discord.com/post_message`
- Updated: 2026-09-18 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/discord.com/post_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/discord.com/post_message
```

## Input

- `channelUrl` (string, required): Full channel URL, e.g. https://discord.com/channels/<guildId>/<channelId>
- `message` (string, optional): Text of the message. Optional when a file is attached, in which case it becomes the message's caption. Discord refuses anything over 2000 characters client-side.
- `filename` (string, optional): Name the file is posted under, e.g. report.csv. Required whenever fileBase64 is given, and used to confirm the attachment Discord stored is the one that was sent.
- `mimeType` (string, optional): Optional content type for the attachment, e.g. text/csv. Guessed from the filename extension when omitted.
- `fileBase64` (string, optional): Optional file to attach, as base64 bytes. Sent as one message together with the text. Keep it small — the request payload limits this to roughly 380 KB of base64, well under Discord's own upload limit.

## Output

- `sent` (boolean, required)
- `content` (string | null, optional): Content as stored by Discord.
- `channelId` (string | null, optional)
- `messageId` (string | null, optional): ID of the created message.
- `timestamp` (string | null, optional)
- `attachment` (object | null, optional): The file Discord stored, read back from its own response — null when no file was sent.

## FAQ

### What does "Post a Discord message" do?

Posts a text message in a Discord channel, addressed by channel URL. Requires being logged in to Discord. Returns `sent` plus the created message's messageId, channelId, timestamp and content as Discord stored it. This is a write: the message appears in the channel and is visible to everyone who can see it. Discord's own message limits are checked before anything is sent, so a message that is empty or whitespace-only, or longer than 2000 characters, is refused straight away with a clear reason.

### How do I automatically post a Discord message on discord.com?

Ask an AI agent connected to Reduck to run reduck/discord.com/post_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/post_message

### Is there a discord.com API to post a Discord message?

You do not need one. "Post a Discord message" drives the real discord.com pages in a browser, so it works whether or not discord.com offers an API for this.

### What information do I need to provide?

Required: channelUrl. Optional: message, filename, mimeType, fileBase64.

### What does it return?

It returns sent, content, channelId, messageId, timestamp, attachment.

### Do I need to be logged in to discord.com?

Yes. It acts as you on discord.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the discord.com cookies saved by the Reduck extension.

### Does it change anything on discord.com, or only read data?

It makes changes on discord.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/discord.com/post_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/post_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/discord.com/post_message
