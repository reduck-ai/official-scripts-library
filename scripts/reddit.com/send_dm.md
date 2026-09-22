# Send Reddit DM

Automatically send Reddit DM on reddit.com. Send a Reddit direct message to a user. Returns sent and recipient. A subject is required by Reddit but won't appear in the conversation. Fails for recipients who don't accept DMs. Runs only via the browser extension, not the hosted cloud browser.

- Site: reddit.com
- Address: `reduck/reddit.com/send_dm`
- Updated: 2026-07-31 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/reddit.com/send_dm`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/reddit.com/send_dm
```

## Input

- `to` (string, required): Recipient username, with or without u/ prefix
- `message` (string, required): Message body (max 10000 chars)
- `subject` (string, required): Message subject/title (max 100 chars); required by the form but not shown in the chat thread

## Output

- `to` (string, required): Recipient username the message was sent to (u/ prefix stripped)
- `sent` (boolean, required): True only when the SendDirectChatToRedditor mutation returned ok

## FAQ

### What does "Send Reddit DM" do?

Send a Reddit direct message to a user. Returns sent and recipient. A subject is required by Reddit but won't appear in the conversation. Fails for recipients who don't accept DMs. Runs only via the browser extension, not the hosted cloud browser.

### How do I automatically send Reddit DM on reddit.com?

Ask an AI agent connected to Reduck to run reduck/reddit.com/send_dm, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/send_dm

### Is there a reddit.com API to send Reddit DM?

You do not need one. "Send Reddit DM" drives the real reddit.com pages in a browser, so it works whether or not reddit.com offers an API for this.

### What information do I need to provide?

Required: to, subject, message.

### What does it return?

It returns to, sent.

### Do I need to be logged in to reddit.com?

Yes. It acts as you on reddit.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the reddit.com cookies saved by the Reduck extension.

### Does it change anything on reddit.com, or only read data?

It makes changes on reddit.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/reddit.com/send_dm, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/send_dm

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/reddit.com/send_dm
