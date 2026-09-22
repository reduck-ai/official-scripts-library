# List Dust agents

Automatically list Dust agents on dust.tt. List the agents available in the signed-in Dust workspace. Returns workspaceId and agents (sId, name, description, scope, status, model provider/id, userFavorite, canEdit, tags). sId is what you pass as `agent` to ask or send_message. Scope tells you where an agent comes from: "global" is a Dust built-in such as dust, helper, deep-dive or analyst, "workspace"/"published" is one your workspace created, "hidden"/"private" is personal. Requires being signed in to dust.tt.

- Site: dust.tt
- Address: `reduck/dust.tt/list_agents`
- Updated: 2026-08-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dust.tt/list_agents`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dust.tt/list_agents
```

## Input

- `workspaceId` (string, optional): Workspace sId. Omit to use the first workspace on the account.

## Output

- `agents` (array, required)
- `workspaceId` (string, required)

## FAQ

### What does "List Dust agents" do?

List the agents available in the signed-in Dust workspace. Returns workspaceId and agents (sId, name, description, scope, status, model provider/id, userFavorite, canEdit, tags). sId is what you pass as `agent` to ask or send_message. Scope tells you where an agent comes from: "global" is a Dust built-in such as dust, helper, deep-dive or analyst, "workspace"/"published" is one your workspace created, "hidden"/"private" is personal. Requires being signed in to dust.tt.

### How do I automatically list Dust agents on dust.tt?

Ask an AI agent connected to Reduck to run reduck/dust.tt/list_agents, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dust.tt/list_agents

### Is there a dust.tt API to list Dust agents?

You do not need one. "List Dust agents" drives the real dust.tt pages in a browser, so it works whether or not dust.tt offers an API for this.

### What information do I need to provide?

Optional: workspaceId.

### What does it return?

It returns agents, workspaceId.

### Do I need to be logged in to dust.tt?

Yes. It acts as you on dust.tt: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the dust.tt cookies saved by the Reduck extension.

### Does it change anything on dust.tt, or only read data?

It only reads. It looks things up on dust.tt and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dust.tt/list_agents, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dust.tt/list_agents

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/dust.tt/list_agents
