# Send a Dust message

Automatically send a Dust message on dust.tt. Send a follow-up message into an existing Dust conversation and wait for the agent's reply (up to 3 minutes). Takes the conversationId from list_conversations, search_conversations or ask. Returns the reply text, the ids of both the sent message and the reply, the agent that answered, and whether generation completed. The agent defaults to "dust"; pass agent to address another one (list_agents). Like ask, this polls rather than streaming, and completed=false means the wait ran out while the agent was still working — the partial reply is returned and the rest can be read later with get_conversation_messages. Only the new reply is returned, not the whole thread: use get_conversation_messages for that.

- Site: dust.tt
- Address: `reduck/dust.tt/send_message`
- Updated: 2026-08-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dust.tt/send_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dust.tt/send_message
```

## Input

- `message` (string, required): The message to send.
- `conversationId` (string, required): Conversation sId to post into, e.g. "P35s1dnqSr".
- `agent` (string, optional): Agent sId to address, e.g. "dust". Defaults to "dust".
- `workspaceId` (string, optional): Workspace sId. Omit to use the first workspace on the account.
- `timeoutSeconds` (integer, optional): How long to wait for the reply (default 180).

## Output

- `url` (string, required)
- `agent` (string, required)
- `reply` (string | null, required): The agent's reply as markdown. Null when the agent produced no text (tool-only or errored turn) — a real outcome, not a parse failure.
- `completed` (boolean, required): False means the wait expired while the agent was still working; the reply is partial.
- `sentMessageId` (string | null, required): sId Dust gave the message that was sent.
- `waitedSeconds` (integer, required)
- `conversationId` (string, required)
- `replyMessageId` (string | null, required): sId of the agent's reply.

## FAQ

### What does "Send a Dust message" do?

Send a follow-up message into an existing Dust conversation and wait for the agent's reply (up to 3 minutes). Takes the conversationId from list_conversations, search_conversations or ask. Returns the reply text, the ids of both the sent message and the reply, the agent that answered, and whether generation completed. The agent defaults to "dust"; pass agent to address another one (list_agents). Like ask, this polls rather than streaming, and completed=false means the wait ran out while the agent was still working — the partial reply is returned and the rest can be read later with get_conversation_messages. Only the new reply is returned, not the whole thread: use get_conversation_messages for that.

### How do I automatically send a Dust message on dust.tt?

Ask an AI agent connected to Reduck to run reduck/dust.tt/send_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dust.tt/send_message

### Is there a dust.tt API to send a Dust message?

You do not need one. "Send a Dust message" drives the real dust.tt pages in a browser, so it works whether or not dust.tt offers an API for this.

### What information do I need to provide?

Required: conversationId, message. Optional: agent, workspaceId, timeoutSeconds.

### What does it return?

It returns url, agent, reply, completed, sentMessageId, waitedSeconds, conversationId, replyMessageId.

### Do I need to be logged in to dust.tt?

Yes. It acts as you on dust.tt: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the dust.tt cookies saved by the Reduck extension.

### Does it change anything on dust.tt, or only read data?

It makes changes on dust.tt, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dust.tt/send_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dust.tt/send_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/dust.tt/send_message
