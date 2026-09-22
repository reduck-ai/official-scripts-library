# Edit Chat Message

Automatically edit Chat Message on teams.microsoft.com. Edit one of your own previously-sent messages in a 1:1 Teams chat, identified by its message id (mid), replacing its text.

- Site: teams.microsoft.com
- Address: `reduck/teams.microsoft.com/edit_chat_message`
- Updated: 2026-09-17 (v12)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/teams.microsoft.com/edit_chat_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/teams.microsoft.com/edit_chat_message
```

## Input

- `mid` (string, required): Message id of your own message to edit — an opaque string, taken verbatim from send_chat_message's output or get_chat_messages. Two formats coexist: older messages carry a 13-digit epoch-ms id (e.g. "1788513273902"), messages sent from mid-September 2026 onward carry a 19-digit id (e.g. "1325909771129090295") that is not a timestamp. Never construct, parse or validate a mid by digit count or as a date; pass through exactly what you read.
- `newText` (string, required): Replacement text for the message.
- `contactName` (string, required): Display name of the person whose 1:1 chat to open, as it appears in Teams (e.g. "April Deere").

## Output

- `mid` (string, required)
- `text` (string | null, required): Text of the message read back after the edit.
- `edited` (boolean, required)

## FAQ

### What does "Edit Chat Message" do?

Edit one of your own previously-sent messages in a 1:1 Teams chat, identified by its message id (mid), replacing its text.

### How do I automatically edit Chat Message on teams.microsoft.com?

Ask an AI agent connected to Reduck to run reduck/teams.microsoft.com/edit_chat_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/teams.microsoft.com/edit_chat_message

### Is there a teams.microsoft.com API to edit Chat Message?

You do not need one. "Edit Chat Message" drives the real teams.microsoft.com pages in a browser, so it works whether or not teams.microsoft.com offers an API for this.

### What information do I need to provide?

Required: contactName, mid, newText.

### What does it return?

It returns mid, text, edited.

### Do I need to be logged in to teams.microsoft.com?

Yes. It acts as you on teams.microsoft.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the teams.microsoft.com cookies saved by the Reduck extension.

### Does it change anything on teams.microsoft.com, or only read data?

It makes changes on teams.microsoft.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/teams.microsoft.com/edit_chat_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/teams.microsoft.com/edit_chat_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/teams.microsoft.com/edit_chat_message
