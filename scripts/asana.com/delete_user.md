# Remove Asana team member

Automatically remove Asana team member on asana.com. Remove a member (by email) from an Asana team, via Team Settings > Members > role dropdown > "Remove from team". Confirms the removal in the dialog that follows. Requires login and team-admin permission.

- Site: asana.com
- Address: `reduck/asana.com/delete_user`
- Updated: 2026-08-31 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/asana.com/delete_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/asana.com/delete_user
```

## Input

- `email` (string, required): Email of the member to remove.
- `teamName` (string, required): Team name as shown in the sidebar (case-insensitive substring match).

## Output

- `team` (string, required)
- `email` (string, required)
- `removed` (boolean, required)

## FAQ

### What does "Remove Asana team member" do?

Remove a member (by email) from an Asana team, via Team Settings > Members > role dropdown > "Remove from team". Confirms the removal in the dialog that follows. Requires login and team-admin permission.

### How do I automatically remove Asana team member on asana.com?

Ask an AI agent connected to Reduck to run reduck/asana.com/delete_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/asana.com/delete_user

### Is there a asana.com API to remove Asana team member?

You do not need one. "Remove Asana team member" drives the real asana.com pages in a browser, so it works whether or not asana.com offers an API for this.

### What information do I need to provide?

Required: teamName, email.

### What does it return?

It returns team, email, removed.

### Do I need to be logged in to asana.com?

Yes. It acts as you on asana.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the asana.com cookies saved by the Reduck extension.

### Does it change anything on asana.com, or only read data?

It makes changes on asana.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/asana.com/delete_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/asana.com/delete_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/asana.com/delete_user
