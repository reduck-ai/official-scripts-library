# Get X DM inbox

Automatically get X DM inbox on x.com. List the state of every DM conversation in your X inbox. Returns per conversation: conversation_id, name, handle, last_message, time, sent_by_me, unread. If X shows the Enter Passcode screen, pass the 4-digit E2E pin.

- Site: x.com
- Address: `reduck/x.com/get_inbox`
- Updated: 2026-09-25 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/get_inbox`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/get_inbox
```

## Input

- `pin` (string, optional): 4-digit E2E passcode — required only if X shows the Enter Passcode screen. Omit otherwise.

## Output

- `conversations` (array, required): One entry per conversation in the inbox, in the order X lists them. Empty when the inbox has no conversations.

## FAQ

### What does "Get X DM inbox" do?

List the state of every DM conversation in your X inbox. Returns per conversation: conversation_id, name, handle, last_message, time, sent_by_me, unread. If X shows the Enter Passcode screen, pass the 4-digit E2E pin.

### How do I automatically get X DM inbox on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/get_inbox, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_inbox

### Is there a x.com API to get X DM inbox?

You do not need one. "Get X DM inbox" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Optional: pin.

### What does it return?

It returns conversations.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It only reads. It looks things up on x.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/get_inbox, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_inbox

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/get_inbox
