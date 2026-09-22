# Invite team member (Stripe)

Automatically invite team member (Stripe) on dashboard.stripe.com. Invite someone into a Stripe team by email, with built-in verification. It records the member list and the pending invitations before and after the action, returning invited / verified / collateralChange — proof the right person was added and nobody else moved. Stripe membership is invite-based: the invitee stays pending until they accept, so this reports an invitation, not an active member. The role you ask for is matched against your account's own role list and defaults to the least privileged one; roles your account is not allowed to grant are reported up front with the list of ones it can. Stripe sometimes asks you to confirm your identity before it will apply a team change — when that happens the invitation is refused and this stops with a clear explanation instead of reporting success, so complete that confirmation in the dashboard and run it again. dryRun (default true) fills the form and stops before sending. Requires being signed into Stripe with team permissions. Pair with dashboard.stripe.com/delete_user, which also cancels a pending invite.

- Site: dashboard.stripe.com
- Address: `reduck/dashboard.stripe.com/create_user`
- Updated: 2026-08-14 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dashboard.stripe.com/create_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dashboard.stripe.com/create_user
```

## Input

- `email` (string, required): Email address to invite to the Stripe team.
- `role` (string, optional): Role name to grant, matched against this account's role list (e.g. "View Only", "Administrator"). Defaults to "View Only".
- `dryRun` (boolean, optional): When true (the default) the invite panel is filled in and then dismissed without sending. Set false to actually send the invite.

## Output

- `email` (string, required)
- `dryRun` (boolean, required)
- `invited` (boolean, required)
- `after` (object, optional)
- `before` (object, optional)
- `verified` (boolean, optional)
- `roleMatched` (string | null, optional)
- `roleRequested` (string, optional)
- `collateralChange` (array, optional)

## FAQ

### What does "Invite team member (Stripe)" do?

Invite someone into a Stripe team by email, with built-in verification. It records the member list and the pending invitations before and after the action, returning invited / verified / collateralChange — proof the right person was added and nobody else moved. Stripe membership is invite-based: the invitee stays pending until they accept, so this reports an invitation, not an active member. The role you ask for is matched against your account's own role list and defaults to the least privileged one; roles your account is not allowed to grant are reported up front with the list of ones it can. Stripe sometimes asks you to confirm your identity before it will apply a team change — when that happens the invitation is refused and this stops with a clear explanation instead of reporting success, so complete that confirmation in the dashboard and run it again. dryRun (default true) fills the form and stops before sending. Requires being signed into Stripe with team permissions. Pair with dashboard.stripe.com/delete_user, which also cancels a pending invite.

### How do I automatically invite team member (Stripe) on dashboard.stripe.com?

Ask an AI agent connected to Reduck to run reduck/dashboard.stripe.com/create_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dashboard.stripe.com/create_user

### Is there a dashboard.stripe.com API to invite team member (Stripe)?

You do not need one. "Invite team member (Stripe)" drives the real dashboard.stripe.com pages in a browser, so it works whether or not dashboard.stripe.com offers an API for this.

### What information do I need to provide?

Required: email. Optional: role, dryRun.

### What does it return?

It returns after, email, before, dryRun, invited, verified, roleMatched, roleRequested, collateralChange.

### Do I need to be logged in to dashboard.stripe.com?

Yes. It acts as you on dashboard.stripe.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the dashboard.stripe.com cookies saved by the Reduck extension.

### Does it change anything on dashboard.stripe.com, or only read data?

It makes changes on dashboard.stripe.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dashboard.stripe.com/create_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dashboard.stripe.com/create_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/dashboard.stripe.com/create_user
