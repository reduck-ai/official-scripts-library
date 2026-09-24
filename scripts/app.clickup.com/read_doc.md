# Read a ClickUp Doc

Automatically read a ClickUp Doc on app.clickup.com. Returns the full text of a ClickUp Doc, page by page, including subpages and where each one sits in the page tree. Accepts the doc's link or its id.

- Site: app.clickup.com
- Address: `reduck/app.clickup.com/read_doc`
- Updated: 2026-09-23 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.clickup.com/read_doc`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/read_doc
```

## Input

- `doc` (string, required): The Doc's link, e.g. https://app.clickup.com/9012345678/docs/abc1234-567, or just its id (abc1234-567). A link to one page of the doc works too — the whole doc is returned either way.
- `workspaceId` (string, optional): Numeric ClickUp workspace id. Only needed when the doc is given as a bare id rather than a link; otherwise it is read from the link.

## Output

- `docId` (string, required)
- `pages` (array, required)
- `pageCount` (number, required)
- `workspaceId` (string, required)
- `url` (string, optional)
- `docName` (string | null, optional): The doc's own name, which ClickUp takes from its first page.
- `accountUsed` (string | null, optional)
- `archivedCount` (number, optional): How many of the returned pages are archived or deleted. They are included rather than dropped, so the count is never silently short.

## FAQ

### What does "Read a ClickUp Doc" do?

Returns the full text of a ClickUp Doc, page by page, including subpages and where each one sits in the page tree. Accepts the doc's link or its id.

### How do I automatically read a ClickUp Doc on app.clickup.com?

Ask an AI agent connected to Reduck to run reduck/app.clickup.com/read_doc, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/read_doc

### Is there a app.clickup.com API to read a ClickUp Doc?

You do not need one. "Read a ClickUp Doc" drives the real app.clickup.com pages in a browser, so it works whether or not app.clickup.com offers an API for this.

### What information do I need to provide?

Required: doc. Optional: workspaceId.

### What does it return?

It returns url, docId, pages, docName, pageCount, accountUsed, workspaceId, archivedCount.

### Do I need to be logged in to app.clickup.com?

Yes. It acts as you on app.clickup.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.clickup.com cookies saved by the Reduck extension.

### Does it change anything on app.clickup.com, or only read data?

It only reads. It looks things up on app.clickup.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.clickup.com/read_doc, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/read_doc

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.clickup.com/read_doc
