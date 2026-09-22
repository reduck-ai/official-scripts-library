# Get X DM messages

Automatically get X DM messages on x.com. Fetch all messages in a DM conversation, addressed by handle or by conversation_id. Returns conversation_id, the other party's handle, and messages with text, sender, direction, date and time. If X shows the Enter Passcode screen, pass the 4-digit E2E pin.

- Site: x.com
- Address: `reduck/x.com/get_messages`
- Updated: 2026-09-03 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/get_messages`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/get_messages
```

## Input

- `pin` (string, optional): 4-digit E2E passcode — required only if X shows the Enter Passcode screen. Omit otherwise.
- `handle` (string, optional): Recipient's X handle, with or without a leading @. Resolved to a user id via the profile page, so it works for any conversation, not just ones already loaded in the inbox.
- `conversationId` (string, optional): conversation_id from get_inbox, e.g. "1667221889486340115-1995746956204015616" (":" separator also accepted). Required for group conversations, whose id is not a user-id pair.

## Output

- `messages` (array, required)
- `conversation_id` (string | null, required)
- `note` (string | null, optional)
- `empty` (boolean, optional): True when the conversation opened but has no rendered messages.
- `participant` (string | null, optional): Handle of the other party, read from the thread header (without @). Null in group conversations.

## FAQ

### What does "Get X DM messages" do?

Fetch all messages in a DM conversation, addressed by handle or by conversation_id. Returns conversation_id, the other party's handle, and messages with text, sender, direction, date and time. If X shows the Enter Passcode screen, pass the 4-digit E2E pin.

### How do I automatically get X DM messages on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/get_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_messages

### Is there a x.com API to get X DM messages?

You do not need one. "Get X DM messages" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Optional: pin, handle, conversationId.

### What does it return?

It returns note, empty, messages, participant, conversation_id.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It only reads. It looks things up on x.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/get_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_messages

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/get_messages
