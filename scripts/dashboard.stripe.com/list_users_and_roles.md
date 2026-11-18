# List Stripe Dashboard team members and roles

Automatically list Stripe Dashboard team members and roles on dashboard.stripe.com. Lists the members of the signed-in Stripe account's team with their name, email and the labels shown next to them: role, owner or inactive flags and last sign-in. Read-only. Fails with a sign-in error when the browser is not signed in to Stripe.

- Site: dashboard.stripe.com
- Address: `reduck/dashboard.stripe.com/list_users_and_roles`
- Updated: 2026-11-17 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dashboard.stripe.com/list_users_and_roles`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dashboard.stripe.com/list_users_and_roles
```

## Input

It takes no input.

## Output

- `count` (number, required)
- `members` (array, required)

## FAQ

### What does "List Stripe Dashboard team members and roles" do?

Lists the members of the signed-in Stripe account's team with their name, email and the labels shown next to them: role, owner or inactive flags and last sign-in. Read-only. Fails with a sign-in error when the browser is not signed in to Stripe.

### How do I automatically list Stripe Dashboard team members and roles on dashboard.stripe.com?

Ask an AI agent connected to Reduck to run reduck/dashboard.stripe.com/list_users_and_roles, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dashboard.stripe.com/list_users_and_roles

### Is there a dashboard.stripe.com API to list Stripe Dashboard team members and roles?

You do not need one. "List Stripe Dashboard team members and roles" drives the real dashboard.stripe.com pages in a browser, so it works whether or not dashboard.stripe.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, members.

### Do I need to be logged in to dashboard.stripe.com?

Yes. It acts as you on dashboard.stripe.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the dashboard.stripe.com cookies saved by the Reduck extension.

### Does it change anything on dashboard.stripe.com, or only read data?

It only reads. It looks things up on dashboard.stripe.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dashboard.stripe.com/list_users_and_roles, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dashboard.stripe.com/list_users_and_roles

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/dashboard.stripe.com/list_users_and_roles
