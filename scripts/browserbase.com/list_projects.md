# Browserbase — list projects

Automatically list projects on browserbase.com. List the projects of a Browserbase organization: each project's id and name, plus the account's role in the org, the project the dashboard opens by default, and the plan's project limit. Pass org (the slug from browserbase.com/whoami) or omit it for the default org. Read-only; signed out is a clear error.

- Site: browserbase.com
- Address: `reduck/browserbase.com/list_projects`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/browserbase.com/list_projects`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/browserbase.com/list_projects
```

## Input

- `org` (string, optional): Browserbase org slug (the /orgs/<slug>/ part of the URL, or an organization slug from browserbase.com/whoami). Omit for the account's default org.

## Output

- `org` (string, required)
- `count` (integer, required)
- `projects` (array, required)
- `role` (string | null, optional)
- `maxProjects` (integer | null, optional)
- `currentProjectId` (string | null, optional)

## FAQ

### What does "Browserbase — list projects" do?

List the projects of a Browserbase organization: each project's id and name, plus the account's role in the org, the project the dashboard opens by default, and the plan's project limit. Pass org (the slug from browserbase.com/whoami) or omit it for the default org. Read-only; signed out is a clear error.

### How do I automatically list projects on browserbase.com?

Ask an AI agent connected to Reduck to run reduck/browserbase.com/list_projects, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/browserbase.com/list_projects

### Is there a browserbase.com API to list projects?

You do not need one. "Browserbase — list projects" drives the real browserbase.com pages in a browser, so it works whether or not browserbase.com offers an API for this.

### What information do I need to provide?

Optional: org.

### What does it return?

It returns org, role, count, projects, maxProjects, currentProjectId.

### Do I need to be logged in to browserbase.com?

Yes. It acts as you on browserbase.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the browserbase.com cookies saved by the Reduck extension.

### Does it change anything on browserbase.com, or only read data?

It only reads. It looks things up on browserbase.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/browserbase.com/list_projects, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/browserbase.com/list_projects

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/browserbase.com/list_projects
