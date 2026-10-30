# Comment on a Pennylane supplier invoice

Automatically comment on a Pennylane supplier invoice on app.pennylane.com. Adds a comment to a Pennylane supplier invoice, in its comment thread, where the company team and the accountant read it. Returns the new comment's id and text, and how many comments the invoice now has, as read back from Pennylane. Fails when the invoice does not exist and when signed out of Pennylane.

- Site: app.pennylane.com
- Address: `reduck/app.pennylane.com/add_invoice_comment`
- Updated: 2026-10-29 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.pennylane.com/add_invoice_comment`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/add_invoice_comment
```

## Input

- `content` (string, required): Text of the comment.
- `companyId` (integer | string, required): The number in the app URL at /companies/<id>/.
- `invoiceId` (integer | string, required): Supplier invoice id, as app.pennylane.com/list_invoices returns it.

## Output

- `content` (string, required)
- `commentId` (string, required)
- `invoiceId` (string, required)
- `label` (string | null, optional)
- `commentsCount` (integer | null, optional): Comments on the invoice after this one, as read back.

## FAQ

### What does "Comment on a Pennylane supplier invoice" do?

Adds a comment to a Pennylane supplier invoice, in its comment thread, where the company team and the accountant read it. Returns the new comment's id and text, and how many comments the invoice now has, as read back from Pennylane. Fails when the invoice does not exist and when signed out of Pennylane.

### How do I automatically comment on a Pennylane supplier invoice on app.pennylane.com?

Ask an AI agent connected to Reduck to run reduck/app.pennylane.com/add_invoice_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/add_invoice_comment

### Is there a app.pennylane.com API to comment on a Pennylane supplier invoice?

You do not need one. "Comment on a Pennylane supplier invoice" drives the real app.pennylane.com pages in a browser, so it works whether or not app.pennylane.com offers an API for this.

### What information do I need to provide?

Required: companyId, invoiceId, content.

### What does it return?

It returns label, content, commentId, invoiceId, commentsCount.

### Do I need to be logged in to app.pennylane.com?

Yes. It acts as you on app.pennylane.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.pennylane.com cookies saved by the Reduck extension.

### Does it change anything on app.pennylane.com, or only read data?

It makes changes on app.pennylane.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.pennylane.com/add_invoice_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/add_invoice_comment

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.pennylane.com/add_invoice_comment
