# WhatsApp — Vote poll

Automatically vote poll on web.whatsapp.com. Cast (or confirm) your vote for one option of a WhatsApp poll, by chat name + poll message id (from get_conversation) + exact option text. Safe to repeat: it does nothing if you already voted for that option. For single-answer polls voting a new option moves your vote; for multi-answer polls it adds one. Verifies the option is checked.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/vote_poll`
- Updated: 2026-08-26 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/vote_poll`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/vote_poll
```

## Input

- `id` (string, required): Poll message id (the id from get_conversation).
- `name` (string, required): Exact chat/contact/group name containing the poll.
- `option` (string, required): Exact text of the option to vote for.

## Output

- `voted` (boolean, required)
- `option` (string, required)
- `recipient` (string, required)

## FAQ

### What does "WhatsApp — Vote poll" do?

Cast (or confirm) your vote for one option of a WhatsApp poll, by chat name + poll message id (from get_conversation) + exact option text. Safe to repeat: it does nothing if you already voted for that option. For single-answer polls voting a new option moves your vote; for multi-answer polls it adds one. Verifies the option is checked.

### How do I automatically vote poll on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/vote_poll, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/vote_poll

### Is there a web.whatsapp.com API to vote poll?

You do not need one. "WhatsApp — Vote poll" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: name, id, option.

### What does it return?

It returns voted, option, recipient.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It makes changes on web.whatsapp.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/vote_poll, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/vote_poll

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/vote_poll
