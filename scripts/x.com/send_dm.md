# Send X DM

Automatically send X DM on x.com. Send a direct message to an X user, addressed by handle. Returns the recipient, a sent flag and conversation_id. Delivery is confirmed by X's own send mutation returning HTTP 200, not by reading the DOM. conversation_id is null for a brand-new DM and for a DM to your own account (the compose dialog renders no existing-conversation cell to read the recipient id from) — a null there does not mean the send failed. A fresh session with no stored encryption keys may need the 4-digit E2E pin.

- Site: x.com
- Address: `reduck/x.com/send_dm`
- Updated: 2026-09-02 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/send_dm`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/send_dm
```

## Input

- `handle` (string, required): Recipient's X handle without @
- `message` (string, required): Message text to send
- `pin` (string, optional): 4-digit E2E passcode — required only if X shows the Enter Passcode screen (fresh session without stored encryption keys). Omit otherwise.

## Output

- `sent` (boolean, required)
- `recipient` (string, required)
- `conversation_id` (string | null, optional): Derived as "<recipientId>-<ownId>", matching get_inbox's format. Null when the compose dialog offered no existing-conversation cell to read the recipient id from — the case for a brand-new DM and for a DM to your own account — so null here does not mean the send failed. Confirm delivery with get_messages if you need it.

## FAQ

### What does "Send X DM" do?

Send a direct message to an X user, addressed by handle. Returns the recipient, a sent flag and conversation_id. Delivery is confirmed by X's own send mutation returning HTTP 200, not by reading the DOM. conversation_id is null for a brand-new DM and for a DM to your own account (the compose dialog renders no existing-conversation cell to read the recipient id from) — a null there does not mean the send failed. A fresh session with no stored encryption keys may need the 4-digit E2E pin.

### How do I automatically send X DM on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/send_dm, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/send_dm

### Is there a x.com API to send X DM?

You do not need one. "Send X DM" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Required: handle, message. Optional: pin.

### What does it return?

It returns sent, recipient, conversation_id.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It makes changes on x.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/send_dm, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/send_dm

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/send_dm
