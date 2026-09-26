# Cancel registration for a Luma event

Automatically cancel registration for a Luma event on luma.com. Cancel the signed-in Luma account's registration for an event by its slug. A registration already cancelled is reported as such rather than an error; an event the account was never registered for is refused, since there is nothing to cancel. This notifies the event organizer that you won't attend, so confirm the event with the person you're helping before running it — re-registering afterward is a separate action.

- Site: luma.com
- Address: `reduck/luma.com/unregister_from_event`
- Updated: 2026-09-25 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/luma.com/unregister_from_event`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/luma.com/unregister_from_event
```

## Input

- `slug` (string, required): The event's short Luma slug, e.g. "9n5kxo7k" from luma.com/9n5kxo7k.

## Output

- `slug` (string, required)
- `event_id` (string, required)
- `already_cancelled` (boolean, required)

## FAQ

### What does "Cancel registration for a Luma event" do?

Cancel the signed-in Luma account's registration for an event by its slug. A registration already cancelled is reported as such rather than an error; an event the account was never registered for is refused, since there is nothing to cancel. This notifies the event organizer that you won't attend, so confirm the event with the person you're helping before running it — re-registering afterward is a separate action.

### How do I automatically cancel registration for a Luma event on luma.com?

Ask an AI agent connected to Reduck to run reduck/luma.com/unregister_from_event, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/luma.com/unregister_from_event

### Is there a luma.com API to cancel registration for a Luma event?

You do not need one. "Cancel registration for a Luma event" drives the real luma.com pages in a browser, so it works whether or not luma.com offers an API for this.

### What information do I need to provide?

Required: slug.

### What does it return?

It returns slug, event_id, already_cancelled.

### Do I need to be logged in to luma.com?

Yes. It acts as you on luma.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the luma.com cookies saved by the Reduck extension.

### Does it change anything on luma.com, or only read data?

It makes changes on luma.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/luma.com/unregister_from_event, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/luma.com/unregister_from_event

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/luma.com/unregister_from_event
