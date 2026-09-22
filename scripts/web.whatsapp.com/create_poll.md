# WhatsApp — Create poll

Automatically create poll on web.whatsapp.com. Send a poll to a WhatsApp chat by exact name: a question plus 2–12 options, with an optional allowMultiple toggle. Works in 1:1 and group chats.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/create_poll`
- Updated: 2026-08-27 (v13)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/create_poll`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/create_poll
```

## Input

- `name` (string, required): Exact chat/contact/group name (the name from get_inbox).
- `options` (array, required): 2 to 12 poll options. They must all be different — WhatsApp rejects a poll with a repeated option, so this is checked before the poll is started.
- `question` (string, required): The poll question.
- `allowMultiple` (boolean, optional): Let voters pick more than one option. False (the default) sends a single-answer poll, which WhatsApp labels "Select one".

## Output

- `sent` (boolean, required)
- `options` (array, required)
- `question` (string, required)
- `recipient` (string, required)

## FAQ

### What does "WhatsApp — Create poll" do?

Send a poll to a WhatsApp chat by exact name: a question plus 2–12 options, with an optional allowMultiple toggle. Works in 1:1 and group chats.

### How do I automatically create poll on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/create_poll, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/create_poll

### Is there a web.whatsapp.com API to create poll?

You do not need one. "WhatsApp — Create poll" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: name, question, options. Optional: allowMultiple.

### What does it return?

It returns sent, options, question, recipient.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It makes changes on web.whatsapp.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/create_poll, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/create_poll

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/create_poll
