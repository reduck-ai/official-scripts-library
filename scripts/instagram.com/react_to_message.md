# React to an Instagram DM message

Automatically react to an Instagram DM message on instagram.com. Add an emoji reaction to a message in an Instagram DM thread. Targets the last message by default, or one identified by message id.

- Site: instagram.com
- Address: `reduck/instagram.com/react_to_message`
- Updated: 2026-08-25 (v14)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/react_to_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/react_to_message
```

## Input

- `username` (string, required): Handle of the conversation partner, without @.
- `messageText` (string, required): Text (or a distinctive fragment) of the message to react to — required to identify which message, since Instagram doesn't expose a stable per-message id.
- `reaction` (string, optional): Emoji to react with. Default ❤️.

## Output

- `status` (string, required): already_reacted = the emoji was already on the message and nothing was written.
- `reaction` (string, required)
- `targetText` (string, required)
- `threadId` (string | null, optional)
- `username` (string, optional)
- `messageId` (string | null, optional): item_id of the message that was reacted to.

## FAQ

### What does "React to an Instagram DM message" do?

Add an emoji reaction to a message in an Instagram DM thread. Targets the last message by default, or one identified by message id.

### How do I automatically react to an Instagram DM message on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/react_to_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/react_to_message

### Is there a instagram.com API to react to an Instagram DM message?

You do not need one. "React to an Instagram DM message" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: username, messageText. Optional: reaction.

### What does it return?

It returns status, reaction, threadId, username, messageId, targetText.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It makes changes on instagram.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/react_to_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/react_to_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/react_to_message
