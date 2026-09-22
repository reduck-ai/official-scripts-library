# List Dust conversations

Automatically list Dust conversations on dust.tt. List the signed-in Dust workspace's conversations, newest first. Returns workspaceId and conversations (sId, title, created, updated, unread, hasError, actionRequired, isRunningAgentLoop, spaceId), plus hasMore and nextCursor for paging. sId is the join key for get_conversation_messages. Pass workspaceId to target a specific workspace when the account belongs to several; it defaults to the first workspace on the account. Paginate with cursor (pass back the nextCursor you were given) rather than an offset — the list is ordered by last update, so an offset would skip or repeat rows as conversations move. Requires being signed in to dust.tt.

- Site: dust.tt
- Address: `reduck/dust.tt/list_conversations`
- Updated: 2026-08-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dust.tt/list_conversations`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dust.tt/list_conversations
```

## Input

- `limit` (integer, optional): Max conversations to return (default 30).
- `cursor` (string, optional): Continue a previous listing: pass the nextCursor returned by an earlier call. Omit for the first page.
- `workspaceId` (string, optional): Workspace sId to read. Omit to use the first workspace on the account (returned as workspaceId so you can pin it).

## Output

- `hasMore` (boolean, required): True when more conversations exist past this page.
- `nextCursor` (string | null, required): Pass as `cursor` to get the next page. Null when hasMore is false.
- `workspaceId` (string, required): The workspace actually read — pass it back as workspaceId to pin subsequent calls.
- `conversations` (array, required)

## FAQ

### What does "List Dust conversations" do?

List the signed-in Dust workspace's conversations, newest first. Returns workspaceId and conversations (sId, title, created, updated, unread, hasError, actionRequired, isRunningAgentLoop, spaceId), plus hasMore and nextCursor for paging. sId is the join key for get_conversation_messages. Pass workspaceId to target a specific workspace when the account belongs to several; it defaults to the first workspace on the account. Paginate with cursor (pass back the nextCursor you were given) rather than an offset — the list is ordered by last update, so an offset would skip or repeat rows as conversations move. Requires being signed in to dust.tt.

### How do I automatically list Dust conversations on dust.tt?

Ask an AI agent connected to Reduck to run reduck/dust.tt/list_conversations, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dust.tt/list_conversations

### Is there a dust.tt API to list Dust conversations?

You do not need one. "List Dust conversations" drives the real dust.tt pages in a browser, so it works whether or not dust.tt offers an API for this.

### What information do I need to provide?

Optional: limit, cursor, workspaceId.

### What does it return?

It returns hasMore, nextCursor, workspaceId, conversations.

### Do I need to be logged in to dust.tt?

Yes. It acts as you on dust.tt: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the dust.tt cookies saved by the Reduck extension.

### Does it change anything on dust.tt, or only read data?

It only reads. It looks things up on dust.tt and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dust.tt/list_conversations, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dust.tt/list_conversations

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/dust.tt/list_conversations
