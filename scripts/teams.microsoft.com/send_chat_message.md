# Send Chat Message

Automatically send Chat Message on teams.microsoft.com. Send a message in a 1:1 Teams chat by contact name — finds the person, opens their chat, sends the message, then reads the sent message back to confirm it posted.

- Site: teams.microsoft.com
- Address: `reduck/teams.microsoft.com/send_chat_message`
- Updated: 2026-09-17 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/teams.microsoft.com/send_chat_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/teams.microsoft.com/send_chat_message
```

## Input

- `message` (string, required): Text to send as the chat message.
- `contactName` (string, required): Display name of the person whose 1:1 chat to open, as it appears in Teams (e.g. "April Deere").

## Output

- `mid` (string | null, required): Message id of the sent message, read back from the chat pane — an OPAQUE string. Two formats coexist in one thread: older messages carry a 13-digit epoch-ms id (e.g. "1788513273902"), messages sent from mid-September 2026 onward carry a 19-digit id (e.g. "1325909771129090295") that is NOT a timestamp. Never parse mid as a date or assume a digit count; pass it verbatim to edit_chat_message, which treats it as opaque.
- `sent` (boolean, required)
- `text` (string | null, required): Text of the sent message, read back from the chat pane.
- `contactName` (string, required)

## FAQ

### What does "Send Chat Message" do?

Send a message in a 1:1 Teams chat by contact name — finds the person, opens their chat, sends the message, then reads the sent message back to confirm it posted.

### How do I automatically send Chat Message on teams.microsoft.com?

Ask an AI agent connected to Reduck to run reduck/teams.microsoft.com/send_chat_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/teams.microsoft.com/send_chat_message

### Is there a teams.microsoft.com API to send Chat Message?

You do not need one. "Send Chat Message" drives the real teams.microsoft.com pages in a browser, so it works whether or not teams.microsoft.com offers an API for this.

### What information do I need to provide?

Required: contactName, message.

### What does it return?

It returns mid, sent, text, contactName.

### Do I need to be logged in to teams.microsoft.com?

Yes. It acts as you on teams.microsoft.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the teams.microsoft.com cookies saved by the Reduck extension.

### Does it change anything on teams.microsoft.com, or only read data?

It makes changes on teams.microsoft.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/teams.microsoft.com/send_chat_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/teams.microsoft.com/send_chat_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/teams.microsoft.com/send_chat_message
