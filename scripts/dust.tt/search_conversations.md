# Search Dust conversations

Automatically search Dust conversations on dust.tt. Search the signed-in Dust workspace's conversations by title text. Returns workspaceId and the matching conversations (sId, title, created, updated, spaceName), newest-updated first, with hasMore and nextCursor. sId is the join key for get_messages. The search covers conversation titles, not message bodies, so a word spoken inside a chat will not match unless it is also in the title — and Dust titles conversations automatically, so titles are paraphrases of the opening message. An empty match list is a real answer about the query, not a failure. Requires being signed in to dust.tt.

- Site: dust.tt
- Address: `reduck/dust.tt/search_conversations`
- Updated: 2026-08-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dust.tt/search_conversations`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dust.tt/search_conversations
```

## Input

- `query` (string, required): Text to look for in conversation titles. Case-insensitive; punctuation is matched literally.
- `limit` (integer, optional): Max matches to return (default 30).
- `cursor` (string, optional): Continue a previous search: pass the nextCursor from an earlier call.
- `workspaceId` (string, optional): Workspace sId to search. Omit to use the first workspace on the account.

## Output

- `query` (string, required): The query actually run, echoed back.
- `hasMore` (boolean, required)
- `nextCursor` (string | null, required): Pass as `cursor` for the next page; null when hasMore is false.
- `workspaceId` (string, required)
- `conversations` (array, required): Matching conversations, newest-updated first. Empty means Dust matched nothing for this query — a fact about the query, not an error.

## FAQ

### What does "Search Dust conversations" do?

Search the signed-in Dust workspace's conversations by title text. Returns workspaceId and the matching conversations (sId, title, created, updated, spaceName), newest-updated first, with hasMore and nextCursor. sId is the join key for get_messages. The search covers conversation titles, not message bodies, so a word spoken inside a chat will not match unless it is also in the title — and Dust titles conversations automatically, so titles are paraphrases of the opening message. An empty match list is a real answer about the query, not a failure. Requires being signed in to dust.tt.

### How do I automatically search Dust conversations on dust.tt?

Ask an AI agent connected to Reduck to run reduck/dust.tt/search_conversations, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dust.tt/search_conversations

### Is there a dust.tt API to search Dust conversations?

You do not need one. "Search Dust conversations" drives the real dust.tt pages in a browser, so it works whether or not dust.tt offers an API for this.

### What information do I need to provide?

Required: query. Optional: limit, cursor, workspaceId.

### What does it return?

It returns query, hasMore, nextCursor, workspaceId, conversations.

### Do I need to be logged in to dust.tt?

Yes. It acts as you on dust.tt: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the dust.tt cookies saved by the Reduck extension.

### Does it change anything on dust.tt, or only read data?

It only reads. It looks things up on dust.tt and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dust.tt/search_conversations, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dust.tt/search_conversations

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/dust.tt/search_conversations
