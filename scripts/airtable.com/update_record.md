# Update an Airtable record

Automatically update an Airtable record on airtable.com. Change field values of one record in an Airtable base and return it as Airtable stored it. Fields you leave out keep their values, a field set to null is emptied, and a field that already holds the value is left alone. Changes text, long text, email, URL, phone, number, currency, percent, checkbox, date and single or multiple select fields. Get record ids from list_records.

- Site: airtable.com
- Address: `reduck/airtable.com/update_record`
- Updated: 2026-11-19 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/airtable.com/update_record`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/airtable.com/update_record
```

## Input

- `baseId` (string, required): Base id (app...), from list_bases or the base's URL.
- `fields` (object, required): New values by field name (or field id); null empties a field. Text, long text, email, URL and phone take a string; number, currency and percent a number; checkbox true or false; date an ISO date (2026-11-03) or date-time; single select an option name; multiple select a list of option names, which replaces the current list; collaborator the email or user id of someone the base is shared with; linked record a list of record ids (rec...) or primary field values, which replaces the current links; attachment a list that replaces the current files: an attachment id (att...) keeps that file, a public file link (or {url, filename}) adds one. Options must already exist.
- `recordId` (string, required): Record id (rec...), from list_records or create_record.

## Output

- `id` (string, required)
- `url` (string, required)
- `table` (object, required)
- `fields` (object, required): The record's values as Airtable stored them, read back after the write.
- `changed` (array, required): Names of the fields whose value changed; a field that already held the value is not sent again.
- `verified` (boolean, required): True when the record was read back with every value given.

## FAQ

### What does "Update an Airtable record" do?

Change field values of one record in an Airtable base and return it as Airtable stored it. Fields you leave out keep their values, a field set to null is emptied, and a field that already holds the value is left alone. Changes text, long text, email, URL, phone, number, currency, percent, checkbox, date and single or multiple select fields. Get record ids from list_records.

### How do I automatically update an Airtable record on airtable.com?

Ask an AI agent connected to Reduck to run reduck/airtable.com/update_record, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/airtable.com/update_record

### Is there a airtable.com API to update an Airtable record?

You do not need one. "Update an Airtable record" drives the real airtable.com pages in a browser, so it works whether or not airtable.com offers an API for this.

### What information do I need to provide?

Required: baseId, recordId, fields.

### What does it return?

It returns id, url, table, fields, changed, verified.

### Do I need to be logged in to airtable.com?

Yes. It acts as you on airtable.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the airtable.com cookies saved by the Reduck extension.

### Does it change anything on airtable.com, or only read data?

It makes changes on airtable.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/airtable.com/update_record, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/airtable.com/update_record

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/airtable.com/update_record
