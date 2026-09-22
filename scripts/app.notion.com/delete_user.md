# Remove workspace member (Notion)

Automatically remove workspace member (Notion) on app.notion.com. Remove a member from a Notion workspace by email, with built-in verification. It records the member list before and after, returning removed / verified / collateralLoss — proof the right person disappeared and nobody else moved. Notion serves one of two different confirmation steps depending on the case, and both are handled. dryRun (default true) dismisses the confirmation without removing; set it to false to go through with it. Acts on the workspace currently active in the browser, so there is no workspace name to pass. Requires being signed into Notion as a workspace owner. Cannot remove the currently signed-in account itself — Notion routes that through a separate "Leave workspace" flow this script doesn't support, and it fails fast with a clear error rather than attempting it.

- Site: app.notion.com
- Address: `reduck/app.notion.com/delete_user`
- Updated: 2026-09-11 (v12)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.notion.com/delete_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.notion.com/delete_user
```

## Input

- `email` (string, required): Email of the workspace member or guest to remove. It must not be the account currently signed into Notion: Notion routes removing yourself through a separate "Leave workspace" flow with its own confirmation dialog, which this script does not support and refuses rather than attempts.
- `dryRun` (boolean, optional): If true (default), walk the whole removal path - including the reason survey and the final confirmation - and dismiss the last dialog without removing. Set false to actually remove.

## Output

- `email` (string, required)
- `found` (boolean, required)
- `dryRun` (boolean, required)
- `removed` (boolean, required)
- `gate` (string | null, optional)
- `role` (string | null, optional)
- `after` (object, optional)
- `before` (object, optional)
- `verified` (boolean, optional)
- `foundInTab` (string | null, optional): Label of the tab the target was found in, for traceability.
- `collateralLoss` (array, optional)

## FAQ

### What does "Remove workspace member (Notion)" do?

Remove a member from a Notion workspace by email, with built-in verification. It records the member list before and after, returning removed / verified / collateralLoss — proof the right person disappeared and nobody else moved. Notion serves one of two different confirmation steps depending on the case, and both are handled. dryRun (default true) dismisses the confirmation without removing; set it to false to go through with it. Acts on the workspace currently active in the browser, so there is no workspace name to pass. Requires being signed into Notion as a workspace owner. Cannot remove the currently signed-in account itself — Notion routes that through a separate "Leave workspace" flow this script doesn't support, and it fails fast with a clear error rather than attempting it.

### How do I automatically remove workspace member (Notion) on app.notion.com?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/delete_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/delete_user

### Is there a app.notion.com API to remove workspace member (Notion)?

You do not need one. "Remove workspace member (Notion)" drives the real app.notion.com pages in a browser, so it works whether or not app.notion.com offers an API for this.

### What information do I need to provide?

Required: email. Optional: dryRun.

### What does it return?

It returns gate, role, after, email, found, before, dryRun, removed, verified, foundInTab, collateralLoss.

### Do I need to be logged in to app.notion.com?

Yes. It acts as you on app.notion.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.notion.com cookies saved by the Reduck extension.

### Does it change anything on app.notion.com, or only read data?

It makes changes on app.notion.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/delete_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/delete_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.notion.com/delete_user
