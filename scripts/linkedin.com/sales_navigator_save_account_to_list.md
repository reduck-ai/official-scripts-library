# Sales Navigator – Save account(s) to list

Automatically save account(s) to list on linkedin.com. Saves one or more LinkedIn Sales Navigator company accounts into a manual account list. Takes account ids (from sales_navigator_search_accounts / sales_navigator_get_account) and a list id (from sales_navigator_list_account_lists), and reports per-account whether it was saved or already present. Mirrors sales_navigator_save_lead_to_list; this changes your account and needs a Sales Navigator seat.

- Site: linkedin.com
- Address: `reduck/linkedin.com/sales_navigator_save_account_to_list`
- Updated: 2026-08-27 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/sales_navigator_save_account_to_list`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_save_account_to_list
```

## Input

- `accountIds` (array, required): Sales Navigator account ids (numeric strings) from search_accounts / get_account.
- `listId` (string, optional): Manual account list id from sales_navigator_list_account_lists. Omit to use the account's default manual list.

## Output

- `results` (array, required)
- `requested` (array, required)
- `httpStatus` (integer, required)
- `listId` (string | null, optional)
- `listName` (string | null, optional)
- `entityCountAfter` (integer | null, optional)
- `entityCountBefore` (integer | null, optional)

## FAQ

### What does "Sales Navigator – Save account(s) to list" do?

Saves one or more LinkedIn Sales Navigator company accounts into a manual account list. Takes account ids (from sales_navigator_search_accounts / sales_navigator_get_account) and a list id (from sales_navigator_list_account_lists), and reports per-account whether it was saved or already present. Mirrors sales_navigator_save_lead_to_list; this changes your account and needs a Sales Navigator seat.

### How do I automatically save account(s) to list on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/sales_navigator_save_account_to_list, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_save_account_to_list

### Is there a linkedin.com API to save account(s) to list?

You do not need one. "Sales Navigator – Save account(s) to list" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: accountIds. Optional: listId.

### What does it return?

It returns listId, results, listName, requested, httpStatus, entityCountAfter, entityCountBefore.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/sales_navigator_save_account_to_list, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_save_account_to_list

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/sales_navigator_save_account_to_list
