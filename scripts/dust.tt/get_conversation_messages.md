# Get Dust conversation messages

Automatically get Dust conversation messages on dust.tt. Read a Dust conversation's messages by conversation sId (from list_conversations or search_conversations), oldest first. Returns workspaceId, conversationId, title, a truncated flag, and messages: each with sId, role (user or agent), content, created, rank, plus author (the human's name/email on a user turn) and agent (the mentioned agent's id on an agent turn). truncated is true when limit stopped it before the first message, so the oldest turns are missing. An unknown conversation id fails loudly rather than returning an empty transcript. Requires being signed in to dust.tt.

- Site: dust.tt
- Address: `reduck/dust.tt/get_conversation_messages`
- Updated: 2026-08-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dust.tt/get_conversation_messages`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dust.tt/get_conversation_messages
```

## Input

- `conversationId` (string, required): Conversation sId, e.g. "P35s1dnqSr" — from list_conversations or search_conversations.
- `limit` (integer, optional): Max messages to return (default 200). The newest are kept when a conversation is longer.
- `workspaceId` (string, optional): Workspace sId. Omit to use the first workspace on the account.

## Output

- `title` (string | null, required): Conversation title, null when Dust has not titled it yet.
- `messages` (array, required): Oldest first — reading order.
- `truncated` (boolean, required): True when `limit` cut the history short, so the oldest messages are not included.
- `workspaceId` (string, required)
- `conversationId` (string, required)

## FAQ

### What does "Get Dust conversation messages" do?

Read a Dust conversation's messages by conversation sId (from list_conversations or search_conversations), oldest first. Returns workspaceId, conversationId, title, a truncated flag, and messages: each with sId, role (user or agent), content, created, rank, plus author (the human's name/email on a user turn) and agent (the mentioned agent's id on an agent turn). truncated is true when limit stopped it before the first message, so the oldest turns are missing. An unknown conversation id fails loudly rather than returning an empty transcript. Requires being signed in to dust.tt.

### How do I automatically get Dust conversation messages on dust.tt?

Ask an AI agent connected to Reduck to run reduck/dust.tt/get_conversation_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dust.tt/get_conversation_messages

### Is there a dust.tt API to get Dust conversation messages?

You do not need one. "Get Dust conversation messages" drives the real dust.tt pages in a browser, so it works whether or not dust.tt offers an API for this.

### What information do I need to provide?

Required: conversationId. Optional: limit, workspaceId.

### What does it return?

It returns title, messages, truncated, workspaceId, conversationId.

### Do I need to be logged in to dust.tt?

Yes. It acts as you on dust.tt: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the dust.tt cookies saved by the Reduck extension.

### Does it change anything on dust.tt, or only read data?

It only reads. It looks things up on dust.tt and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dust.tt/get_conversation_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dust.tt/get_conversation_messages

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/dust.tt/get_conversation_messages
