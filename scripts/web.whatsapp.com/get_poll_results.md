# WhatsApp — Get poll results

Automatically get poll results on web.whatsapp.com. Read the current results of a WhatsApp poll, by chat name plus the poll message's id. Returns the poll question, whether it accepts more than one answer per person, each option with its vote count, and which options the signed-in account has voted for. Reading a poll changes nothing and notifies nobody. Older polls are found by loading further back through the conversation. Individual voter names are not included — only the counts. Pairs with the poll creating and voting scripts.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/get_poll_results`
- Updated: 2026-09-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/get_poll_results`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_poll_results
```

## Input

- `id` (string, required): The poll message's id, as returned by get_conversation or search_messages.
- `name` (string, required): Exact chat name containing the poll, as returned by get_inbox.

## Output

- `id` (string, required)
- `chat` (string, required): The chat the poll was read from, echoed from the conversation header.
- `options` (array, required)
- `question` (string | null, required)
- `totalVotes` (integer, required): Sum of the per-option counts. On a multi-answer poll one person can add several, so this is not necessarily the number of people who voted.
- `allowMultiple` (boolean, required): True when the poll accepts more than one answer per person.

## FAQ

### What does "WhatsApp — Get poll results" do?

Read the current results of a WhatsApp poll, by chat name plus the poll message's id. Returns the poll question, whether it accepts more than one answer per person, each option with its vote count, and which options the signed-in account has voted for. Reading a poll changes nothing and notifies nobody. Older polls are found by loading further back through the conversation. Individual voter names are not included — only the counts. Pairs with the poll creating and voting scripts.

### How do I automatically get poll results on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/get_poll_results, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_poll_results

### Is there a web.whatsapp.com API to get poll results?

You do not need one. "WhatsApp — Get poll results" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: name, id.

### What does it return?

It returns id, chat, options, question, totalVotes, allowMultiple.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It only reads. It looks things up on web.whatsapp.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/get_poll_results, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_poll_results

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/get_poll_results
