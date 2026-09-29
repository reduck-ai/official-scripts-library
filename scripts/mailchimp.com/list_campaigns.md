# Mailchimp — list campaigns

Automatically list campaigns on mailchimp.com. List the email campaigns in the signed-in Mailchimp account (All campaigns): each campaign's internal and public id, name, type, status (draft/save, schedule, sending, sent…), audience and segment, created and updated dates, edit link and public archive link. Returns the list the page loads (its first page). Read-only; signed out is a clear error.

- Site: mailchimp.com
- Address: `reduck/mailchimp.com/list_campaigns`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mailchimp.com/list_campaigns`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mailchimp.com/list_campaigns
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `campaigns` (array, required)
- `dataCenter` (string | null, optional)

## FAQ

### What does "Mailchimp — list campaigns" do?

List the email campaigns in the signed-in Mailchimp account (All campaigns): each campaign's internal and public id, name, type, status (draft/save, schedule, sending, sent…), audience and segment, created and updated dates, edit link and public archive link. Returns the list the page loads (its first page). Read-only; signed out is a clear error.

### How do I automatically list campaigns on mailchimp.com?

Ask an AI agent connected to Reduck to run reduck/mailchimp.com/list_campaigns, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mailchimp.com/list_campaigns

### Is there a mailchimp.com API to list campaigns?

You do not need one. "Mailchimp — list campaigns" drives the real mailchimp.com pages in a browser, so it works whether or not mailchimp.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, campaigns, dataCenter.

### Do I need to be logged in to mailchimp.com?

Yes. It acts as you on mailchimp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mailchimp.com cookies saved by the Reduck extension.

### Does it change anything on mailchimp.com, or only read data?

It only reads. It looks things up on mailchimp.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mailchimp.com/list_campaigns, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mailchimp.com/list_campaigns

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/mailchimp.com/list_campaigns
