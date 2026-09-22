# Delete a Dust conversation

Automatically delete a Dust conversation on dust.tt. Delete a Dust conversation by its sId — the inverse of ask, for cleaning up conversations a script created. Returns the title it had, deleted, and verified: the conversation is re-read after the delete, so verified:true means it is genuinely gone rather than merely that the request returned 200. A conversation that was already absent comes back as alreadyAbsent:true with deleted:false, so a no-op is never reported as a successful delete. This is destructive and Dust offers no undo — the conversation and its whole message history go.

- Site: dust.tt
- Address: `reduck/dust.tt/delete_conversation`
- Updated: 2026-08-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dust.tt/delete_conversation`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dust.tt/delete_conversation
```

## Input

- `conversationId` (string, required): Conversation sId to delete, e.g. "GTxrhtUjON".
- `workspaceId` (string, optional): Workspace sId. Omit to use the first workspace on the account.

## Output

- `title` (string | null, required): Title the conversation had before deletion, for the audit trail. Null when it had none or was already absent.
- `deleted` (boolean, required): True only when this call actually removed a conversation that existed.
- `verified` (boolean, required): True when a follow-up read confirmed the conversation is gone. False with deleted:true means Dust accepted the delete but still serves the conversation — treat that as unfinished, not as success.
- `workspaceId` (string, required)
- `alreadyAbsent` (boolean, required): True when there was nothing to delete: the id does not exist in this workspace.
- `conversationId` (string, required)

## FAQ

### What does "Delete a Dust conversation" do?

Delete a Dust conversation by its sId — the inverse of ask, for cleaning up conversations a script created. Returns the title it had, deleted, and verified: the conversation is re-read after the delete, so verified:true means it is genuinely gone rather than merely that the request returned 200. A conversation that was already absent comes back as alreadyAbsent:true with deleted:false, so a no-op is never reported as a successful delete. This is destructive and Dust offers no undo — the conversation and its whole message history go.

### How do I automatically delete a Dust conversation on dust.tt?

Ask an AI agent connected to Reduck to run reduck/dust.tt/delete_conversation, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dust.tt/delete_conversation

### Is there a dust.tt API to delete a Dust conversation?

You do not need one. "Delete a Dust conversation" drives the real dust.tt pages in a browser, so it works whether or not dust.tt offers an API for this.

### What information do I need to provide?

Required: conversationId. Optional: workspaceId.

### What does it return?

It returns title, deleted, verified, workspaceId, alreadyAbsent, conversationId.

### Do I need to be logged in to dust.tt?

Yes. It acts as you on dust.tt: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the dust.tt cookies saved by the Reduck extension.

### Does it change anything on dust.tt, or only read data?

It makes changes on dust.tt, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dust.tt/delete_conversation, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dust.tt/delete_conversation

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/dust.tt/delete_conversation
