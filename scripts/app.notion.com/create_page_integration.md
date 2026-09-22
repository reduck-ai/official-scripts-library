# Create Notion page integration

Automatically create Notion page integration on app.notion.com. Create an internal Notion integration scoped to a specific page and connect it to that page. Returns token, integrationId, pageId, integrationName. The token is shown only at creation, so capture it immediately.

- Site: app.notion.com
- Address: `reduck/app.notion.com/create_page_integration`
- Updated: 2026-09-17 (v23)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.notion.com/create_page_integration`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.notion.com/create_page_integration
```

## Input

- `pageUrl` (string, required): URL of the Notion page to scope and connect the integration to (the page id is extracted from it).
- `integrationName` (string, required): Display name for the new internal integration.
- `workspace` (string, optional): Workspace name the integration must be created under. Notion no longer offers an in-dialog workspace picker, so this must match the workspace currently active in the browser's sidebar - the script validates this upfront and throws if they differ. Default: the currently active workspace.
- `capabilities` (array, optional): Integration capabilities. Default ['read'].

## Output

- `token` (string, required)
- `pageId` (string, required)
- `connected` (boolean, required): Whether the integration was confirmed among the page's active connections on a fresh read after being added. Always true on a successful run: the script throws rather than returning if it cannot see the connection, because the integration and its token are created before this step and a silent failure would leave a live credential connected to nothing.
- `workspace` (string, required)
- `integrationId` (string, required)
- `integrationName` (string, required)

## FAQ

### What does "Create Notion page integration" do?

Create an internal Notion integration scoped to a specific page and connect it to that page. Returns token, integrationId, pageId, integrationName. The token is shown only at creation, so capture it immediately.

### How do I automatically create Notion page integration on app.notion.com?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/create_page_integration, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/create_page_integration

### Is there a app.notion.com API to create Notion page integration?

You do not need one. "Create Notion page integration" drives the real app.notion.com pages in a browser, so it works whether or not app.notion.com offers an API for this.

### What information do I need to provide?

Required: pageUrl, integrationName. Optional: workspace, capabilities.

### What does it return?

It returns token, pageId, connected, workspace, integrationId, integrationName.

### Do I need to be logged in to app.notion.com?

Yes. It acts as you on app.notion.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.notion.com cookies saved by the Reduck extension.

### Does it change anything on app.notion.com, or only read data?

It makes changes on app.notion.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/create_page_integration, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/create_page_integration

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.notion.com/create_page_integration
