# Create an Airtable record

Automatically create an Airtable record on airtable.com. Add a record to a table of an Airtable base, with the field values you give, and return it as Airtable stored it. Fills text, long text, email, URL, phone, number, currency, percent, checkbox, date and single or multiple select fields; select options must already exist. list_records shows each field's name, type and options.

- Site: airtable.com
- Address: `reduck/airtable.com/create_record`
- Updated: 2026-11-19 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/airtable.com/create_record`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/airtable.com/create_record
```

## Input

- `baseId` (string, required): Base id (app...), from list_bases or the base's URL.
- `fields` (object, required): Values by field name (or field id). Text, long text, email, URL and phone take a string; number, currency and percent a number; checkbox true or false; date an ISO date (2026-11-03) or date-time; single select an option name; multiple select a list of option names; collaborator the email or user id of someone the base is shared with; linked record a list of record ids (rec...) or primary field values of the linked table; attachment a list of public file links (or {url, filename}), which Airtable downloads and stores.
- `table` (string, optional): Table name or id (tbl...). Leave it out for the base's first table.

## Output

- `id` (string, required): The new record's id (rec...).
- `url` (string, required)
- `table` (object, required)
- `fields` (object, required): The record's values as Airtable stored them, read back after the write.
- `verified` (boolean, required): True when the record was read back from the base with every value given.
- `createdTime` (string | null, required)

## FAQ

### What does "Create an Airtable record" do?

Add a record to a table of an Airtable base, with the field values you give, and return it as Airtable stored it. Fills text, long text, email, URL, phone, number, currency, percent, checkbox, date and single or multiple select fields; select options must already exist. list_records shows each field's name, type and options.

### How do I automatically create an Airtable record on airtable.com?

Ask an AI agent connected to Reduck to run reduck/airtable.com/create_record, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/airtable.com/create_record

### Is there a airtable.com API to create an Airtable record?

You do not need one. "Create an Airtable record" drives the real airtable.com pages in a browser, so it works whether or not airtable.com offers an API for this.

### What information do I need to provide?

Required: baseId, fields. Optional: table.

### What does it return?

It returns id, url, table, fields, verified, createdTime.

### Do I need to be logged in to airtable.com?

Yes. It acts as you on airtable.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the airtable.com cookies saved by the Reduck extension.

### Does it change anything on airtable.com, or only read data?

It makes changes on airtable.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/airtable.com/create_record, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/airtable.com/create_record

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/airtable.com/create_record
