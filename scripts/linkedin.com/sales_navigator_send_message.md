# Sales Navigator — send message (regular, by recipient name)

Automatically send message (regular, by recipient name) on linkedin.com. Send a regular message (no InMail, subject, or credit) from the LinkedIn Sales Navigator inbox to a 1st/2nd-degree connection, found by name. It picks the first typeahead match for the name, so recipientResolved echoes the chosen suggestion; confirm it's the right person before relying on the result. The inbox composer only reaches your connections; out-of-network leads need InMail from the lead page instead. Needs a Sales Navigator seat. This is the Sales Navigator inbox, not classic LinkedIn messaging.

- Site: linkedin.com
- Address: `reduck/linkedin.com/sales_navigator_send_message`
- Updated: 2026-08-26 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/sales_navigator_send_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_send_message
```

## Input

- `message` (string, required): Message body to send.
- `recipientName` (string, required): Lead name to type into the recipient typeahead. The first suggestion is picked, so pass a full, unambiguous name; a partial name can resolve to a stranger. Only 1st-degree connections can receive a regular Sales Navigator message.
- `dryRun` (boolean, optional): When true, fill the composer and resolve the real Send control, then stop without clicking it. Nothing is sent. May leave an unsent draft in the composer.

## Output

- `status` (string, required): "sent" means the createMessage call returned OK. "dry_run" means Send was resolved but never clicked.
- `message` (string, required)
- `sendAnchor` (object, required): How the Send control was identified, for diagnostics only — never a selector.
- `recipientName` (string, required): The name that was typed.
- `recipientResolved` (string | null, required): The typeahead entry actually picked, including its degree. Check this: a partial name can resolve to someone else.

## FAQ

### What does "Sales Navigator — send message (regular, by recipient name)" do?

Send a regular message (no InMail, subject, or credit) from the LinkedIn Sales Navigator inbox to a 1st/2nd-degree connection, found by name. It picks the first typeahead match for the name, so recipientResolved echoes the chosen suggestion; confirm it's the right person before relying on the result. The inbox composer only reaches your connections; out-of-network leads need InMail from the lead page instead. Needs a Sales Navigator seat. This is the Sales Navigator inbox, not classic LinkedIn messaging.

### How do I automatically send message (regular, by recipient name) on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/sales_navigator_send_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_send_message

### Is there a linkedin.com API to send message (regular, by recipient name)?

You do not need one. "Sales Navigator — send message (regular, by recipient name)" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: recipientName, message. Optional: dryRun.

### What does it return?

It returns status, message, sendAnchor, recipientName, recipientResolved.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/sales_navigator_send_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_send_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/sales_navigator_send_message
