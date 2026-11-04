# List Neon organization members and roles

Automatically list Neon organization members and roles on console.neon.tech. Lists the members and pending invites of the Neon organization the console opens for the signed-in account, with role, status, join or invite date and whether MFA is on.

- Site: console.neon.tech
- Address: `reduck/console.neon.tech/list_users_and_roles`
- Updated: 2026-11-03 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/console.neon.tech/list_users_and_roles`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/console.neon.tech/list_users_and_roles
```

## Input

It takes no input.

## Output

- `org` (string, required)
- `count` (integer, required)
- `members` (array, required)

## FAQ

### What does "List Neon organization members and roles" do?

Lists the members and pending invites of the Neon organization the console opens for the signed-in account, with role, status, join or invite date and whether MFA is on.

### How do I automatically list Neon organization members and roles on console.neon.tech?

Ask an AI agent connected to Reduck to run reduck/console.neon.tech/list_users_and_roles, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/console.neon.tech/list_users_and_roles

### Is there a console.neon.tech API to list Neon organization members and roles?

You do not need one. "List Neon organization members and roles" drives the real console.neon.tech pages in a browser, so it works whether or not console.neon.tech offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns org, count, members.

### Do I need to be logged in to console.neon.tech?

Yes. It acts as you on console.neon.tech: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the console.neon.tech cookies saved by the Reduck extension.

### Does it change anything on console.neon.tech, or only read data?

It only reads. It looks things up on console.neon.tech and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/console.neon.tech/list_users_and_roles, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/console.neon.tech/list_users_and_roles

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/console.neon.tech/list_users_and_roles
