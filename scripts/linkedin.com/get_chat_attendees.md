# Get LinkedIn conversation attendees

Automatically get LinkedIn conversation attendees on linkedin.com. List the participants of a classic LinkedIn messaging conversation (NOT Sales Navigator) by thread URL from list_inbox — mainly useful for group chats. Returns each attendee's name, profile URL and member urn, plus whether the thread is a group.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_chat_attendees`
- Updated: 2026-09-15 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_chat_attendees`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_chat_attendees
```

## Input

- `threadUrl` (string, required): URL of the conversation thread, e.g. https://www.linkedin.com/messaging/thread/<id>/ (from list_inbox)

## Output

- `count` (integer, required)
- `attendees` (array, required)
- `threadUrl` (string, required)
- `source` (string, optional): Which payload the roster came from. conversationParticipants is the authoritative thread roster; messageActors is a fallback built from who has spoken.
- `threadId` (string | null, optional)
- `groupChat` (boolean | null, optional): True when the roster holds more than two people (including the viewer).

## FAQ

### What does "Get LinkedIn conversation attendees" do?

List the participants of a classic LinkedIn messaging conversation (NOT Sales Navigator) by thread URL from list_inbox — mainly useful for group chats. Returns each attendee's name, profile URL and member urn, plus whether the thread is a group.

### How do I automatically get LinkedIn conversation attendees on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_chat_attendees, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_chat_attendees

### Is there a linkedin.com API to get LinkedIn conversation attendees?

You do not need one. "Get LinkedIn conversation attendees" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: threadUrl.

### What does it return?

It returns count, source, threadId, attendees, groupChat, threadUrl.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_chat_attendees, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_chat_attendees

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_chat_attendees
