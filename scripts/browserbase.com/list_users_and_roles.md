# List Browserbase organization members and roles

Automatically list Browserbase organization members and roles on browserbase.com. Lists the members of a Browserbase organization with their email and the labels shown next to them: project access, role and join date. Pass org (the slug from browserbase.com/whoami) or omit it for the default org. Read-only. Fails with a sign-in error when the browser is not signed in to Browserbase.

- Site: browserbase.com
- Address: `reduck/browserbase.com/list_users_and_roles`
- Updated: 2026-11-17 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/browserbase.com/list_users_and_roles`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/browserbase.com/list_users_and_roles
```

## Input

- `org` (string, optional): Organization slug from browserbase.com/whoami. Omit for the default org.

## Output

- `org` (string, required)
- `count` (number, required)
- `members` (array, required)

## FAQ

### What does "List Browserbase organization members and roles" do?

Lists the members of a Browserbase organization with their email and the labels shown next to them: project access, role and join date. Pass org (the slug from browserbase.com/whoami) or omit it for the default org. Read-only. Fails with a sign-in error when the browser is not signed in to Browserbase.

### How do I automatically list Browserbase organization members and roles on browserbase.com?

Ask an AI agent connected to Reduck to run reduck/browserbase.com/list_users_and_roles, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/browserbase.com/list_users_and_roles

### Is there a browserbase.com API to list Browserbase organization members and roles?

You do not need one. "List Browserbase organization members and roles" drives the real browserbase.com pages in a browser, so it works whether or not browserbase.com offers an API for this.

### What information do I need to provide?

Optional: org.

### What does it return?

It returns org, count, members.

### Do I need to be logged in to browserbase.com?

Yes. It acts as you on browserbase.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the browserbase.com cookies saved by the Reduck extension.

### Does it change anything on browserbase.com, or only read data?

It only reads. It looks things up on browserbase.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/browserbase.com/list_users_and_roles, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/browserbase.com/list_users_and_roles

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/browserbase.com/list_users_and_roles
