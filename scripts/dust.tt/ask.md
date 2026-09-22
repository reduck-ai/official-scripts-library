# Ask Dust

Automatically ask Dust on dust.tt. Start a new Dust conversation, send one question to an agent, and wait for the answer to finish (up to 3 minutes). Returns the answer text, the conversation and message ids, the conversation URL, which agent answered, and whether generation completed. Requires a signed-in dust.tt session. The agent defaults to "dust", the workspace's general-purpose agent; pass agent to address another one by its sId (list them with list_agents). Dust answers asynchronously, so this polls the conversation until the agent's turn stops changing: completed=false means the 3-minute budget ran out while the agent was still working, and the partial answer is returned rather than an error — re-read it later with get_conversation_messages using the conversationId. This creates a real conversation in the workspace; delete it with delete_conversation if it was only a test.

- Site: dust.tt
- Address: `reduck/dust.tt/ask`
- Updated: 2026-08-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dust.tt/ask`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dust.tt/ask
```

## Input

- `question` (string, required): The question to send as the first message of a new conversation.
- `agent` (string, optional): Agent sId to ask, e.g. "dust" (general purpose) or "helper" (help on using Dust). Defaults to "dust".
- `workspaceId` (string, optional): Workspace sId to create the conversation in. Omit to use the first workspace on the account.
- `timeoutSeconds` (integer, optional): How long to wait for the agent to finish (default 180).

## Output

- `url` (string, required): Link to the conversation in the Dust web app.
- `agent` (string, required): The agent that answered, as its sId.
- `answer` (string | null, required): The agent's answer as the markdown it emitted. Null when the agent produced no text at all — which happens on a tool-only or errored turn and is a real outcome, not a parse failure.
- `completed` (boolean, required): True when the agent's turn finished inside the timeout. False means the answer is partial — re-read it later with get_conversation_messages.
- `messageId` (string | null, required): sId of the agent's message.
- `waitedSeconds` (integer, required): How long the poll actually waited before returning.
- `conversationId` (string, required): Conversation sId — the join key for get_conversation_messages.
- `userMessageId` (string | null, optional): sId of the question as Dust stored it.

## FAQ

### What does "Ask Dust" do?

Start a new Dust conversation, send one question to an agent, and wait for the answer to finish (up to 3 minutes). Returns the answer text, the conversation and message ids, the conversation URL, which agent answered, and whether generation completed. Requires a signed-in dust.tt session. The agent defaults to "dust", the workspace's general-purpose agent; pass agent to address another one by its sId (list them with list_agents). Dust answers asynchronously, so this polls the conversation until the agent's turn stops changing: completed=false means the 3-minute budget ran out while the agent was still working, and the partial answer is returned rather than an error — re-read it later with get_conversation_messages using the conversationId. This creates a real conversation in the workspace; delete it with delete_conversation if it was only a test.

### How do I automatically ask Dust on dust.tt?

Ask an AI agent connected to Reduck to run reduck/dust.tt/ask, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dust.tt/ask

### Is there a dust.tt API to ask Dust?

You do not need one. "Ask Dust" drives the real dust.tt pages in a browser, so it works whether or not dust.tt offers an API for this.

### What information do I need to provide?

Required: question. Optional: agent, workspaceId, timeoutSeconds.

### What does it return?

It returns url, agent, answer, completed, messageId, userMessageId, waitedSeconds, conversationId.

### Do I need to be logged in to dust.tt?

Yes. It acts as you on dust.tt: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the dust.tt cookies saved by the Reduck extension.

### Does it change anything on dust.tt, or only read data?

It makes changes on dust.tt, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dust.tt/ask, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dust.tt/ask

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/dust.tt/ask
