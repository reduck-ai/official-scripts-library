# Gmail — Apply or remove a label on a thread

Automatically apply or remove a label on a thread on mail.google.com. Apply a label to a Gmail thread by its hex threadId, optionally creating the label first, or take the label off again with remove:true. A thread already in the requested state is reported as a no-op without clicking. Takes a received thread — Gmail renders no conversation heading for a thread you sent to yourself, so those are refused rather than risk labelling the wrong thread.

- Site: mail.google.com
- Address: `reduck/mail.google.com/add_label`
- Updated: 2026-09-07 (v17)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mail.google.com/add_label`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mail.google.com/add_label
```

## Input

- `label` (string, required): The label name, matched exactly against the account's labels. Exactness matters, because Gmail's own picker offers to create "Lunch" even when "Lunch Bill" exists, so a partial name would quietly make a second label. Gmail's category names (Social, Updates, Forums, Promotions) appear in the same menu but are not user labels.
- `threadId` (string, required): The thread's hex id, as returned by mail.google.com/search_emails (its threadId field, Gmail's data-legacy-thread-id). Note that list_inbox does not return thread ids. Must be a received thread: Gmail does not render a conversation heading for a thread you sent to yourself, and those are refused rather than risk labelling the wrong thread.
- `create` (boolean, optional): Allow creating the label when the account does not have it. Default false, so a typo fails loudly instead of quietly making a new label. Ignored when remove is true.
- `remove` (boolean, optional): Leave false (the default) to apply the label. Set true to take it off.
- `account` (string, optional): Optional authuser value for a browser signed into several Google accounts. Omit for the default (u/0).

## Output

- `label` (string, required)
- `applied` (boolean, required): Whether the thread carries the label after this run, read from a Gmail label search rather than the label menu, which does not report applied state in conversation view.
- `threadId` (string, required)
- `already_present` (boolean, required): True when the thread was already in the requested state, so nothing was written.
- `created` (boolean, optional)
- `attempts` (integer, optional): How many click attempts the toggle needed before Gmail's own label search agreed. More than 1 means a click silently failed to reach the server and was retried.
- `accountUsed` (string | null, optional)
- `verified_by` (any, optional): 'search' when the outcome was confirmed against Gmail's own label search; 'unconfirmed' when the label holds more threads than the first search page, so absence could not be told apart from paging.
- `availableLabels` (array, optional)
- `sync_acknowledged` (boolean, optional): Whether Gmail's own sync write was observed for this toggle.

## FAQ

### What does "Gmail — Apply or remove a label on a thread" do?

Apply a label to a Gmail thread by its hex threadId, optionally creating the label first, or take the label off again with remove:true. A thread already in the requested state is reported as a no-op without clicking. Takes a received thread — Gmail renders no conversation heading for a thread you sent to yourself, so those are refused rather than risk labelling the wrong thread.

### How do I automatically apply or remove a label on a thread on mail.google.com?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/add_label, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/add_label

### Is there a mail.google.com API to apply or remove a label on a thread?

You do not need one. "Gmail — Apply or remove a label on a thread" drives the real mail.google.com pages in a browser, so it works whether or not mail.google.com offers an API for this.

### What information do I need to provide?

Required: threadId, label. Optional: create, remove, account.

### What does it return?

It returns label, applied, created, attempts, threadId, accountUsed, verified_by, already_present, availableLabels, sync_acknowledged.

### Do I need to be logged in to mail.google.com?

Yes. It acts as you on mail.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mail.google.com cookies saved by the Reduck extension.

### Does it change anything on mail.google.com, or only read data?

It makes changes on mail.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/add_label, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/add_label

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/mail.google.com/add_label
