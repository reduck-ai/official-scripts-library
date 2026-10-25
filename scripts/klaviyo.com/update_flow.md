# Rename Klaviyo flow

Automatically rename Klaviyo flow on klaviyo.com. Rename a Klaviyo flow by its flowId from list_flows, then read it back to confirm. It never changes the flow's status, so a draft stays a draft and nothing is sent. Pass dryRun to see the current and new name without changing anything.

- Site: klaviyo.com
- Address: `reduck/klaviyo.com/update_flow`
- Updated: 2026-10-22 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/klaviyo.com/update_flow`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/klaviyo.com/update_flow
```

## Input

- `name` (string, required): New flow name.
- `flowId` (string, required): Flow id from list_flows.
- `dryRun` (boolean, optional): true returns the current and new name without renaming.

## Output

- `name` (string, required)
- `flowId` (string, required)
- `updated` (boolean, required)
- `dryRun` (boolean, optional)
- `status` (string, optional)
- `updatedAt` (string, optional)
- `previousName` (string, optional)

## FAQ

### What does "Rename Klaviyo flow" do?

Rename a Klaviyo flow by its flowId from list_flows, then read it back to confirm. It never changes the flow's status, so a draft stays a draft and nothing is sent. Pass dryRun to see the current and new name without changing anything.

### How do I automatically rename Klaviyo flow on klaviyo.com?

Ask an AI agent connected to Reduck to run reduck/klaviyo.com/update_flow, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/klaviyo.com/update_flow

### Is there a klaviyo.com API to rename Klaviyo flow?

You do not need one. "Rename Klaviyo flow" drives the real klaviyo.com pages in a browser, so it works whether or not klaviyo.com offers an API for this.

### What information do I need to provide?

Required: flowId, name. Optional: dryRun.

### What does it return?

It returns name, dryRun, flowId, status, updated, updatedAt, previousName.

### Do I need to be logged in to klaviyo.com?

Yes. It acts as you on klaviyo.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the klaviyo.com cookies saved by the Reduck extension.

### Does it change anything on klaviyo.com, or only read data?

It makes changes on klaviyo.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/klaviyo.com/update_flow, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/klaviyo.com/update_flow

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/klaviyo.com/update_flow
