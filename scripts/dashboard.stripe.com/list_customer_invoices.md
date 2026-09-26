# List Stripe customer invoices

Automatically list Stripe customer invoices on dashboard.stripe.com. List the invoices your Stripe account has issued to its customers, from the signed-in Stripe dashboard: number, status, customer name and email, amount due, total, currency, creation and due dates, and the hosted invoice link. Choose live or test mode and optionally a status (draft, open, paid, uncollectible, void). Returns the first page of the list and says whether more exist. Reports which mode was actually shown, since Stripe opens test mode on accounts not yet activated for live payments.

- Site: dashboard.stripe.com
- Address: `reduck/dashboard.stripe.com/list_customer_invoices`
- Updated: 2026-09-25 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dashboard.stripe.com/list_customer_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dashboard.stripe.com/list_customer_invoices
```

## Input

- `mode` (string, optional): Which Stripe environment to read. An account not yet activated for live payments only has test data.
- `status` (string, optional): Only invoices in this status.

## Output

- `mode` (string, required): The environment actually shown. Stripe opens test mode when live is not available, and this reports that.
- `count` (number, required): 0 is a real answer: no invoices match.
- `invoices` (array, required)
- `accountId` (string | null, required)
- `hasMore` (boolean, optional): More invoices exist beyond this first page of the list.

## FAQ

### What does "List Stripe customer invoices" do?

List the invoices your Stripe account has issued to its customers, from the signed-in Stripe dashboard: number, status, customer name and email, amount due, total, currency, creation and due dates, and the hosted invoice link. Choose live or test mode and optionally a status (draft, open, paid, uncollectible, void). Returns the first page of the list and says whether more exist. Reports which mode was actually shown, since Stripe opens test mode on accounts not yet activated for live payments.

### How do I automatically list Stripe customer invoices on dashboard.stripe.com?

Ask an AI agent connected to Reduck to run reduck/dashboard.stripe.com/list_customer_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dashboard.stripe.com/list_customer_invoices

### Is there a dashboard.stripe.com API to list Stripe customer invoices?

You do not need one. "List Stripe customer invoices" drives the real dashboard.stripe.com pages in a browser, so it works whether or not dashboard.stripe.com offers an API for this.

### What information do I need to provide?

Optional: mode, status.

### What does it return?

It returns mode, count, hasMore, invoices, accountId.

### Do I need to be logged in to dashboard.stripe.com?

Yes. It acts as you on dashboard.stripe.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the dashboard.stripe.com cookies saved by the Reduck extension.

### Does it change anything on dashboard.stripe.com, or only read data?

It only reads. It looks things up on dashboard.stripe.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dashboard.stripe.com/list_customer_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dashboard.stripe.com/list_customer_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/dashboard.stripe.com/list_customer_invoices
