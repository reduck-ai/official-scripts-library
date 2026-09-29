# Mailchimp — list audiences

Automatically list audiences on mailchimp.com. List the audiences (lists) in the signed-in Mailchimp account: each audience's internal id, public list id (the one Mailchimp's API and signup forms use), name, creation date and whether SMS / WhatsApp are enabled, plus the account's data center. Read-only; signed out is a clear error.

- Site: mailchimp.com
- Address: `reduck/mailchimp.com/list_audiences`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mailchimp.com/list_audiences`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mailchimp.com/list_audiences
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `audiences` (array, required)
- `dataCenter` (string | null, optional)

## FAQ

### What does "Mailchimp — list audiences" do?

List the audiences (lists) in the signed-in Mailchimp account: each audience's internal id, public list id (the one Mailchimp's API and signup forms use), name, creation date and whether SMS / WhatsApp are enabled, plus the account's data center. Read-only; signed out is a clear error.

### How do I automatically list audiences on mailchimp.com?

Ask an AI agent connected to Reduck to run reduck/mailchimp.com/list_audiences, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mailchimp.com/list_audiences

### Is there a mailchimp.com API to list audiences?

You do not need one. "Mailchimp — list audiences" drives the real mailchimp.com pages in a browser, so it works whether or not mailchimp.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, audiences, dataCenter.

### Do I need to be logged in to mailchimp.com?

Yes. It acts as you on mailchimp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mailchimp.com cookies saved by the Reduck extension.

### Does it change anything on mailchimp.com, or only read data?

It only reads. It looks things up on mailchimp.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mailchimp.com/list_audiences, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mailchimp.com/list_audiences

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/mailchimp.com/list_audiences
