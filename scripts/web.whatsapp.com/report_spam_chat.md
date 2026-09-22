# Report spam chat

Automatically report spam chat on web.whatsapp.com. Reports a chat to WhatsApp (sends its last 5 messages to WhatsApp trust &amp; safety), optionally blocking it too.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/report_spam_chat`
- Updated: 2026-09-22 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/report_spam_chat`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/report_spam_chat
```

## Input

- `chatName` (string, required): Name of the chat to report, as it appears in the chat list search.
- `block` (boolean, optional): Also block the chat when reporting it. Defaults to false (report only).

## Output

- `blocked` (boolean, required): True if the block checkbox was also set.
- `reported` (boolean, required): True once the report dialog was submitted.

## FAQ

### What does "Report spam chat" do?

Reports a chat to WhatsApp (sends its last 5 messages to WhatsApp trust &amp; safety), optionally blocking it too.

### How do I automatically report spam chat on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/report_spam_chat, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/report_spam_chat

### Is there a web.whatsapp.com API to report spam chat?

You do not need one. "Report spam chat" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: chatName. Optional: block.

### What does it return?

It returns blocked, reported.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It makes changes on web.whatsapp.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/report_spam_chat, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/report_spam_chat

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/report_spam_chat
