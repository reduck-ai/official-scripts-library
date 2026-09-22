# React to a LinkedIn message

Automatically react to a LinkedIn message on linkedin.com. Add an emoji reaction to a message in a classic LinkedIn messaging thread (NOT Sales Navigator). Targets the last message in the thread by default, or the most recent one containing given text.

- Site: linkedin.com
- Address: `reduck/linkedin.com/react_to_message`
- Updated: 2026-08-25 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/react_to_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/react_to_message
```

## Input

- `threadUrl` (string, required): URL of the conversation thread (from list_inbox).
- `reaction` (string, optional): Emoji to react with. Supported: 👍 (thumbs up, default), 👏 (clapping hands), 😊 (smiling face). Other emoji require LinkedIn's emoji keyboard, which this version does not drive.
- `messageUrn` (string, optional): Exact message identifier, if you have it (as returned by this script's or get_message_attachment's own output). Most precise targeting.
- `messageText` (string, optional): Target the most recent message containing this text. Ignored if messageUrn is given.

## Output

- `status` (string, required)
- `reaction` (string, required)
- `messageUrn` (string, required): Message identifier for the message reacted to — pass it back for precise repeat targeting.
- `threadUrl` (string, optional)
- `targetText` (string | null, optional)

## FAQ

### What does "React to a LinkedIn message" do?

Add an emoji reaction to a message in a classic LinkedIn messaging thread (NOT Sales Navigator). Targets the last message in the thread by default, or the most recent one containing given text.

### How do I automatically react to a LinkedIn message on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/react_to_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/react_to_message

### Is there a linkedin.com API to react to a LinkedIn message?

You do not need one. "React to a LinkedIn message" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: threadUrl. Optional: reaction, messageUrn, messageText.

### What does it return?

It returns status, reaction, threadUrl, messageUrn, targetText.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/react_to_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/react_to_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/react_to_message
