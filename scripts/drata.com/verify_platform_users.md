# List Drata platform users

Automatically list Drata platform users on drata.com. List the users of the signed-in Drata workspace (Settings, Role administration): each user's email, first and last name, roles, date added and last login, plus a total. Pass an email to also learn whether that person is still listed, e.g. to confirm an offboarding went through. Needs a Drata session. Read-only: it never changes a user or a role.

- Site: drata.com
- Address: `reduck/drata.com/verify_platform_users`
- Updated: 2026-10-08 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/drata.com/verify_platform_users`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/drata.com/verify_platform_users
```

## Input

- `email` (string, optional): Optional email to look for; the result then says whether it is listed.

## Output

- `count` (integer, required)
- `users` (array, required)
- `total` (integer, optional)
- `present` (boolean | null, optional)
- `checkedEmail` (string | null, optional)
- `workspaceSlug` (string | null, optional)

## FAQ

### What does "List Drata platform users" do?

List the users of the signed-in Drata workspace (Settings, Role administration): each user's email, first and last name, roles, date added and last login, plus a total. Pass an email to also learn whether that person is still listed, e.g. to confirm an offboarding went through. Needs a Drata session. Read-only: it never changes a user or a role.

### How do I automatically list Drata platform users on drata.com?

Ask an AI agent connected to Reduck to run reduck/drata.com/verify_platform_users, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drata.com/verify_platform_users

### Is there a drata.com API to list Drata platform users?

You do not need one. "List Drata platform users" drives the real drata.com pages in a browser, so it works whether or not drata.com offers an API for this.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns count, total, users, present, checkedEmail, workspaceSlug.

### Do I need to be logged in to drata.com?

Yes. It acts as you on drata.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the drata.com cookies saved by the Reduck extension.

### Does it change anything on drata.com, or only read data?

It only reads. It looks things up on drata.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/drata.com/verify_platform_users, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drata.com/verify_platform_users

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/drata.com/verify_platform_users
