# Find a ClickUp list by name

Automatically find a ClickUp list by name on app.clickup.com. Looks up ClickUp lists by name and returns each match with its identifier and its full location, so a list name can be turned into the identifier other ClickUp scripts need. Every match is returned rather than one being guessed at.

- Site: app.clickup.com
- Address: `reduck/app.clickup.com/find_list`
- Updated: 2026-09-23 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.clickup.com/find_list`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/find_list
```

## Input

- `name` (string, required): The list name to look for. Matching ignores case and surrounding spaces. An exact match wins; if there is none, lists containing the text are returned instead.
- `workspaceId` (string, optional): Numeric ClickUp workspace id. Omit to use whichever workspace ClickUp opens by default.

## Output

- `query` (string, required)
- `matches` (array, required)
- `matchType` (string, required)
- `matchCount` (integer, required)
- `totalLists` (integer, required)
- `workspaceId` (string, required)

## FAQ

### What does "Find a ClickUp list by name" do?

Looks up ClickUp lists by name and returns each match with its identifier and its full location, so a list name can be turned into the identifier other ClickUp scripts need. Every match is returned rather than one being guessed at.

### How do I automatically find a ClickUp list by name on app.clickup.com?

Ask an AI agent connected to Reduck to run reduck/app.clickup.com/find_list, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/find_list

### Is there a app.clickup.com API to find a ClickUp list by name?

You do not need one. "Find a ClickUp list by name" drives the real app.clickup.com pages in a browser, so it works whether or not app.clickup.com offers an API for this.

### What information do I need to provide?

Required: name. Optional: workspaceId.

### What does it return?

It returns query, matches, matchType, matchCount, totalLists, workspaceId.

### Do I need to be logged in to app.clickup.com?

Yes. It acts as you on app.clickup.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.clickup.com cookies saved by the Reduck extension.

### Does it change anything on app.clickup.com, or only read data?

It only reads. It looks things up on app.clickup.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.clickup.com/find_list, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/find_list

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.clickup.com/find_list
