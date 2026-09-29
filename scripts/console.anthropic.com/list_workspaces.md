# Anthropic Console — list workspaces

Automatically list workspaces on console.anthropic.com. List the workspaces of an Anthropic Console (platform.claude.com) organization: workspace id, name, creation date, archived date, data-residency region and display colour. Pass organizationUuid (from console.anthropic.com/whoami) to pick an organization; omit it to use the account's first one. Read-only. An organization without Console access is reported by name rather than as an empty list, and signed out is a clear error.

- Site: console.anthropic.com
- Address: `reduck/console.anthropic.com/list_workspaces`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/console.anthropic.com/list_workspaces`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/console.anthropic.com/list_workspaces
```

## Input

- `organizationUuid` (string, optional): Organization uuid (from console.anthropic.com/whoami). Omit to use the first organization the account belongs to.

## Output

- `count` (integer, required)
- `workspaces` (array, required)
- `organizationUuid` (string, required)
- `organizationName` (string | null, optional)

## FAQ

### What does "Anthropic Console — list workspaces" do?

List the workspaces of an Anthropic Console (platform.claude.com) organization: workspace id, name, creation date, archived date, data-residency region and display colour. Pass organizationUuid (from console.anthropic.com/whoami) to pick an organization; omit it to use the account's first one. Read-only. An organization without Console access is reported by name rather than as an empty list, and signed out is a clear error.

### How do I automatically list workspaces on console.anthropic.com?

Ask an AI agent connected to Reduck to run reduck/console.anthropic.com/list_workspaces, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/console.anthropic.com/list_workspaces

### Is there a console.anthropic.com API to list workspaces?

You do not need one. "Anthropic Console — list workspaces" drives the real console.anthropic.com pages in a browser, so it works whether or not console.anthropic.com offers an API for this.

### What information do I need to provide?

Optional: organizationUuid.

### What does it return?

It returns count, workspaces, organizationName, organizationUuid.

### Do I need to be logged in to console.anthropic.com?

Yes. It acts as you on console.anthropic.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the console.anthropic.com cookies saved by the Reduck extension.

### Does it change anything on console.anthropic.com, or only read data?

It only reads. It looks things up on console.anthropic.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/console.anthropic.com/list_workspaces, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/console.anthropic.com/list_workspaces

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/console.anthropic.com/list_workspaces
