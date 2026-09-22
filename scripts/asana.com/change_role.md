# Change Asana team member's role

Automatically change Asana team member's role on asana.com. Change a team member's role (Team admin / Member), identified by email, via Team Settings > Members > role dropdown. Fails loudly if the target role is disabled for that member (e.g. Asana blocks guests from outside the org's domain from becoming Team admin). Requires login and team-admin permission. Returns the role before and after the change.

- Site: asana.com
- Address: `reduck/asana.com/change_role`
- Updated: 2026-08-20 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/asana.com/change_role`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/asana.com/change_role
```

## Input

- `role` (string, required): New role. Note: guests outside the org's domain cannot be set to 'Team admin' — Asana disables this and the script throws.
- `email` (string, required): Email of the member to change.
- `teamName` (string, required): Team name as shown in the sidebar (case-insensitive substring match).

## Output

- `team` (string, required)
- `email` (string, required)
- `newRole` (string, required)
- `previousRole` (string, required)

## FAQ

### What does "Change Asana team member's role" do?

Change a team member's role (Team admin / Member), identified by email, via Team Settings > Members > role dropdown. Fails loudly if the target role is disabled for that member (e.g. Asana blocks guests from outside the org's domain from becoming Team admin). Requires login and team-admin permission. Returns the role before and after the change.

### How do I automatically change Asana team member's role on asana.com?

Ask an AI agent connected to Reduck to run reduck/asana.com/change_role, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/asana.com/change_role

### Is there a asana.com API to change Asana team member's role?

You do not need one. "Change Asana team member's role" drives the real asana.com pages in a browser, so it works whether or not asana.com offers an API for this.

### What information do I need to provide?

Required: teamName, email, role.

### What does it return?

It returns team, email, newRole, previousRole.

### Do I need to be logged in to asana.com?

Yes. It acts as you on asana.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the asana.com cookies saved by the Reduck extension.

### Does it change anything on asana.com, or only read data?

It makes changes on asana.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/asana.com/change_role, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/asana.com/change_role

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/asana.com/change_role
