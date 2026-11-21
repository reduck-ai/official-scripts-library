# List all ClickUp lists in a workspace

Automatically list all ClickUp lists in a workspace on app.clickup.com. Returns every list in a ClickUp workspace with its identifier, link, space and folder, so a list name can be turned into the identifier other ClickUp scripts need. Lists that sit directly in a space have no folder. Choosing a list by name is left to the caller.

- Site: app.clickup.com
- Address: `reduck/app.clickup.com/find_list`
- Updated: 2026-11-20 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.clickup.com/find_list`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/find_list
```

## Input

- `workspaceId` (string, optional): Numeric ClickUp workspace id. Omit to use whichever workspace ClickUp opens by default.

## Output

- `lists` (array, required)
- `totalLists` (integer, required)
- `workspaceId` (string, required)

## FAQ

### What does "List all ClickUp lists in a workspace" do?

Returns every list in a ClickUp workspace with its identifier, link, space and folder, so a list name can be turned into the identifier other ClickUp scripts need. Lists that sit directly in a space have no folder. Choosing a list by name is left to the caller.

### How do I automatically list all ClickUp lists in a workspace on app.clickup.com?

Ask an AI agent connected to Reduck to run reduck/app.clickup.com/find_list, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/find_list

### Is there a app.clickup.com API to list all ClickUp lists in a workspace?

You do not need one. "List all ClickUp lists in a workspace" drives the real app.clickup.com pages in a browser, so it works whether or not app.clickup.com offers an API for this.

### What information do I need to provide?

Optional: workspaceId.

### What does it return?

It returns lists, totalLists, workspaceId.

### Do I need to be logged in to app.clickup.com?

Yes. It acts as you on app.clickup.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.clickup.com cookies saved by the Reduck extension.

### Does it change anything on app.clickup.com, or only read data?

It only reads. It looks things up on app.clickup.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.clickup.com/find_list, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/find_list

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.clickup.com/find_list
