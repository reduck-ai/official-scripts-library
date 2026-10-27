# List your X (Twitter) DM inbox

Automatically list your X (Twitter) DM inbox on x.com. List the conversations in your X chat inbox, in the order X shows them. Returns per conversation: conversation_id, name, handle, last_message, time, sent_by_me (null in a group conversation) and unread. An empty inbox returns an empty list. If X asks for your chat passcode on this browser, pass the 4-digit passcode as pin; without it the run fails with an error asking for it. When the browser is signed out of X, the run fails with a signed-out error asking you to sign in to x.com.

- Site: x.com
- Address: `reduck/x.com/get_inbox`
- Updated: 2026-10-22 (v10)
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

### What does "List your X (Twitter) DM inbox" do?

List the conversations in your X chat inbox, in the order X shows them. Returns per conversation: conversation_id, name, handle, last_message, time, sent_by_me (null in a group conversation) and unread. An empty inbox returns an empty list. If X asks for your chat passcode on this browser, pass the 4-digit passcode as pin; without it the run fails with an error asking for it. When the browser is signed out of X, the run fails with a signed-out error asking you to sign in to x.com.

### How do I automatically list your X (Twitter) DM inbox on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/get_inbox, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_inbox

### Is there a x.com API to list your X (Twitter) DM inbox?

You do not need one. "List your X (Twitter) DM inbox" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

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
