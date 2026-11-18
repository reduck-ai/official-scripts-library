# Check payments on Pennylane expense claims

Automatically check payments on Pennylane expense claims on app.pennylane.com. Reads the current status, paid flag, pending payments and last payment of the given Pennylane expense claims (companyId, expenseIds), so you can see whether a claim was already reimbursed by transfer before paying it again. Only reads; it never reimburses or sends a payment.

- Site: app.pennylane.com
- Address: `reduck/app.pennylane.com/check_expense_payments`
- Updated: 2026-11-17 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.pennylane.com/check_expense_payments`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/check_expense_payments
```

## Input

- `companyId` (integer | string, required): Pennylane company id, the number in the app URL at /companies/<id>/.
- `expenseIds` (array, required): Ids of the expense claims to check.

## Output

- `claims` (array, required)

## FAQ

### What does "Check payments on Pennylane expense claims" do?

Reads the current status, paid flag, pending payments and last payment of the given Pennylane expense claims (companyId, expenseIds), so you can see whether a claim was already reimbursed by transfer before paying it again. Only reads; it never reimburses or sends a payment.

### How do I automatically check payments on Pennylane expense claims on app.pennylane.com?

Ask an AI agent connected to Reduck to run reduck/app.pennylane.com/check_expense_payments, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/check_expense_payments

### Is there a app.pennylane.com API to check payments on Pennylane expense claims?

You do not need one. "Check payments on Pennylane expense claims" drives the real app.pennylane.com pages in a browser, so it works whether or not app.pennylane.com offers an API for this.

### What information do I need to provide?

Required: companyId, expenseIds.

### What does it return?

It returns claims.

### Do I need to be logged in to app.pennylane.com?

Yes. It acts as you on app.pennylane.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.pennylane.com cookies saved by the Reduck extension.

### Does it change anything on app.pennylane.com, or only read data?

It only reads. It looks things up on app.pennylane.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.pennylane.com/check_expense_payments, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/check_expense_payments

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.pennylane.com/check_expense_payments
