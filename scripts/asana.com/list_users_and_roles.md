# List Asana team members and roles

Automatically list Asana team members and roles on asana.com. List a team's members with email, name, role (Team admin/Member), guest status, and pending-invite status, via the team's Settings > Members panel. Requires login and visibility into the team.

- Site: asana.com
- Address: `reduck/asana.com/list_users_and_roles`
- Updated: 2026-08-20 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/asana.com/list_users_and_roles`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/asana.com/list_users_and_roles
```

## Input

- `teamName` (string, required): Team name as shown in the sidebar (case-insensitive substring match), e.g. 'Marketing'.

## Output

- `team` (string, required)
- `members` (array, required)

## FAQ

### What does "List Asana team members and roles" do?

List a team's members with email, name, role (Team admin/Member), guest status, and pending-invite status, via the team's Settings > Members panel. Requires login and visibility into the team.

### How do I automatically list Asana team members and roles on asana.com?

Ask an AI agent connected to Reduck to run reduck/asana.com/list_users_and_roles, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/asana.com/list_users_and_roles

### Is there a asana.com API to list Asana team members and roles?

You do not need one. "List Asana team members and roles" drives the real asana.com pages in a browser, so it works whether or not asana.com offers an API for this.

### What information do I need to provide?

Required: teamName.

### What does it return?

It returns team, members.

### Do I need to be logged in to asana.com?

Yes. It acts as you on asana.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the asana.com cookies saved by the Reduck extension.

### Does it change anything on asana.com, or only read data?

It only reads. It looks things up on asana.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/asana.com/list_users_and_roles, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/asana.com/list_users_and_roles

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/asana.com/list_users_and_roles
