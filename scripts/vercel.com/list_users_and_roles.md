# List Vercel team members and roles

Automatically list Vercel team members and roles on vercel.com. List a Vercel team's members with their username, email and role. Read-only — changes nothing. Pass the optional email arg to also get a present true/false verdict for that address, which is the quick way to confirm an offboarding landed. team is required (the team's URL slug). Requires being signed into Vercel. Complements vercel.com/delete_user, which already snapshots the member list before and after its own action.

- Site: vercel.com
- Address: `reduck/vercel.com/list_users_and_roles`
- Updated: 2026-07-30 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/vercel.com/list_users_and_roles`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/vercel.com/list_users_and_roles
```

## Input

- `team` (string, required): Vercel team URL slug, e.g. "acme-inc"
- `email` (string, optional): Optional email to check for presence/absence

## Output

- `team` (string, required)
- `count` (number, required)
- `members` (array, required)
- `present` (boolean | null, optional)
- `checkedEmail` (string | null, optional)

## FAQ

### What does "List Vercel team members and roles" do?

List a Vercel team's members with their username, email and role. Read-only — changes nothing. Pass the optional email arg to also get a present true/false verdict for that address, which is the quick way to confirm an offboarding landed. team is required (the team's URL slug). Requires being signed into Vercel. Complements vercel.com/delete_user, which already snapshots the member list before and after its own action.

### How do I automatically list Vercel team members and roles on vercel.com?

Ask an AI agent connected to Reduck to run reduck/vercel.com/list_users_and_roles, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/vercel.com/list_users_and_roles

### Is there a vercel.com API to list Vercel team members and roles?

You do not need one. "List Vercel team members and roles" drives the real vercel.com pages in a browser, so it works whether or not vercel.com offers an API for this.

### What information do I need to provide?

Required: team. Optional: email.

### What does it return?

It returns team, count, members, present, checkedEmail.

### Do I need to be logged in to vercel.com?

Yes. It acts as you on vercel.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the vercel.com cookies saved by the Reduck extension.

### Does it change anything on vercel.com, or only read data?

Unknown: its author has not declared whether it changes anything on vercel.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/vercel.com/list_users_and_roles, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/vercel.com/list_users_and_roles

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/vercel.com/list_users_and_roles
