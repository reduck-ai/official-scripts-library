# Remove team member (Stripe)

Automatically remove team member (Stripe) on dashboard.stripe.com. Remove a member from a Stripe team by email, or cancel an invitation they never accepted — both cases are handled. It records the member list before and after, returning removed / verified / collateralLoss: proof the right person disappeared and nobody else moved. As a safety guard, the destructive click only fires when the confirmation dialog names the target email. It also reports the person's role and their last sign-in date, which is what reveals access still being used after someone left. dryRun (default true) reaches the confirmation step then backs out. Requires being signed into Stripe with team permissions.

- Site: dashboard.stripe.com
- Address: `reduck/dashboard.stripe.com/delete_user`
- Updated: 2026-08-28 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dashboard.stripe.com/delete_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dashboard.stripe.com/delete_user
```

## Input

- `email` (string, required): Email address of the team member or pending invite to remove.
- `dryRun` (boolean, optional): When true (the default) the confirmation modal is opened, checked against the target email, then dismissed without removing. Set false to actually remove.

## Output

- `email` (string, required)
- `found` (boolean, required)
- `dryRun` (boolean, required)
- `removed` (boolean, required)
- `role` (string | null, optional)
- `after` (object, optional)
- `before` (object, optional)
- `verified` (boolean, optional)
- `lastSignIn` (string | null, optional)
- `collateralLoss` (array, optional)
- `wasPendingInvite` (boolean | null, optional)

## FAQ

### What does "Remove team member (Stripe)" do?

Remove a member from a Stripe team by email, or cancel an invitation they never accepted — both cases are handled. It records the member list before and after, returning removed / verified / collateralLoss: proof the right person disappeared and nobody else moved. As a safety guard, the destructive click only fires when the confirmation dialog names the target email. It also reports the person's role and their last sign-in date, which is what reveals access still being used after someone left. dryRun (default true) reaches the confirmation step then backs out. Requires being signed into Stripe with team permissions.

### How do I automatically remove team member (Stripe) on dashboard.stripe.com?

Ask an AI agent connected to Reduck to run reduck/dashboard.stripe.com/delete_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dashboard.stripe.com/delete_user

### Is there a dashboard.stripe.com API to remove team member (Stripe)?

You do not need one. "Remove team member (Stripe)" drives the real dashboard.stripe.com pages in a browser, so it works whether or not dashboard.stripe.com offers an API for this.

### What information do I need to provide?

Required: email. Optional: dryRun.

### What does it return?

It returns role, after, email, found, before, dryRun, removed, verified, lastSignIn, collateralLoss, wasPendingInvite.

### Do I need to be logged in to dashboard.stripe.com?

Yes. It acts as you on dashboard.stripe.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the dashboard.stripe.com cookies saved by the Reduck extension.

### Does it change anything on dashboard.stripe.com, or only read data?

It makes changes on dashboard.stripe.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dashboard.stripe.com/delete_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dashboard.stripe.com/delete_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/dashboard.stripe.com/delete_user
