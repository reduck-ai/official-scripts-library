# Shopify Admin whoami (signed-in account)

Report which store this browser's Shopify admin opens: the store handle, the store's name and the store's contact email (not the signed-in user's own identity). When the browser is not signed in to the Shopify admin, the run fails with a signed-out error that says to sign in, so it can be used to check a session before running other Shopify admin scripts.

- Site: admin.shopify.com
- Address: `reduck/admin.shopify.com/whoami`
- Updated: 2026-10-22 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/admin.shopify.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `name` (string | null, optional): Store name.
- `email` (string | null, optional): Store contact email.
- `store` (string | null, optional): Store handle from admin.shopify.com/store/<handle>.

## FAQ

### What does "Shopify Admin whoami (signed-in account)" do?

Report which store this browser's Shopify admin opens: the store handle, the store's name and the store's contact email (not the signed-in user's own identity). When the browser is not signed in to the Shopify admin, the run fails with a signed-out error that says to sign in, so it can be used to check a session before running other Shopify admin scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email, store, evidence, loggedIn.

### Do I need to be logged in to admin.shopify.com?

Yes. It acts as you on admin.shopify.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the admin.shopify.com cookies saved by the Reduck extension.

### Does it change anything on admin.shopify.com, or only read data?

It only reads. It looks things up on admin.shopify.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/admin.shopify.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/admin.shopify.com/whoami
