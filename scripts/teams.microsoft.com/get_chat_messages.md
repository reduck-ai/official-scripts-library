# Get Chat Messages

Automatically get Chat Messages on teams.microsoft.com. Read messages from a 1:1 Teams chat by contact name. Finds the person, opens their chat, and returns every currently-loaded message with sender, ISO timestamp and text. Needs no admin or export permission.

- Site: teams.microsoft.com
- Address: `reduck/teams.microsoft.com/get_chat_messages`
- Updated: 2026-09-09 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/teams.microsoft.com/get_chat_messages`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/teams.microsoft.com/get_chat_messages
```

## Input

- `contactName` (string, required): Display name of the person whose 1:1 chat to open, as it appears in Teams (e.g. "April Deere").

## Output

- `messages` (array, required)
- `contactName` (string, required)

## FAQ

### What does "Get Chat Messages" do?

Read messages from a 1:1 Teams chat by contact name. Finds the person, opens their chat, and returns every currently-loaded message with sender, ISO timestamp and text. Needs no admin or export permission.

### How do I automatically get Chat Messages on teams.microsoft.com?

Ask an AI agent connected to Reduck to run reduck/teams.microsoft.com/get_chat_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/teams.microsoft.com/get_chat_messages

### Is there a teams.microsoft.com API to get Chat Messages?

You do not need one. "Get Chat Messages" drives the real teams.microsoft.com pages in a browser, so it works whether or not teams.microsoft.com offers an API for this.

### What information do I need to provide?

Required: contactName.

### What does it return?

It returns messages, contactName.

### Do I need to be logged in to teams.microsoft.com?

Yes. It acts as you on teams.microsoft.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the teams.microsoft.com cookies saved by the Reduck extension.

### Does it change anything on teams.microsoft.com, or only read data?

It only reads. It looks things up on teams.microsoft.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/teams.microsoft.com/get_chat_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/teams.microsoft.com/get_chat_messages

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/teams.microsoft.com/get_chat_messages
