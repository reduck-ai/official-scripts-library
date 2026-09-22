# Shopify store admin login (Google SSO)

Log into a Shopify store admin via Google SSO — clicks 'Continue with Google' on accounts.shopify.com, picks the account, skips the passkey-enrollment prompt if shown, then opens admin.shopify.com/store/<store>. Pass the store handle.

- Site: admin.shopify.com
- Address: `reduck/admin.shopify.com/login_with_google`
- Updated: 2026-08-21 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/admin.shopify.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/login_with_google
```

## Input

- `store` (string, required): Shopify store handle as it appears in admin.shopify.com/store/<store> (e.g. "my-shop"). Must be a store your Google account can access.
- `email` (string, optional): Google account to pick in the chooser. Omit to use the first/only account.

## Output

- `url` (string, required)
- `store` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional)
- `already` (boolean, optional): true if a Shopify session already existed (no Google click needed)

## FAQ

### What does "Shopify store admin login (Google SSO)" do?

Log into a Shopify store admin via Google SSO — clicks 'Continue with Google' on accounts.shopify.com, picks the account, skips the passkey-enrollment prompt if shown, then opens admin.shopify.com/store/<store>. Pass the store handle.

### What information do I need to provide?

Required: store. Optional: email.

### What does it return?

It returns url, store, account, already, loggedIn.

### Do I need to be logged in to admin.shopify.com?

Yes. It acts as you on admin.shopify.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the admin.shopify.com cookies saved by the Reduck extension.

### Does it change anything on admin.shopify.com, or only read data?

It makes changes on admin.shopify.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/admin.shopify.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/admin.shopify.com/login_with_google
