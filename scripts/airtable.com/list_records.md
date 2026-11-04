# List Airtable records

Automatically list Airtable records on airtable.com. List the records of one table in an Airtable base, with every field's value, plus the table's fields (name, type and select options) and the base's other tables. Pick the table by name or id; without one, the base's first table is read. Get base ids from list_bases.

- Site: airtable.com
- Address: `reduck/airtable.com/list_records`
- Updated: 2026-11-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/airtable.com/list_records`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/airtable.com/list_records
```

## Input

- `baseId` (string, required): Base id (app...), from list_bases or the base's URL.
- `table` (string, optional): Table name or id (tbl...). Leave it out for the base's first table.
- `maxRecords` (integer, optional): Most records to return, in the table's own order.

## Output

- `base` (object, required)
- `table` (object, required)
- `total` (integer, required): How many records the table holds.
- `fields` (array, required): The table's fields in order, the primary field first.
- `tables` (array, required): Every table of the base, to pick another one.
- `records` (array, required)
- `truncated` (boolean, required): True when the table holds more records than maxRecords.

## FAQ

### What does "List Airtable records" do?

List the records of one table in an Airtable base, with every field's value, plus the table's fields (name, type and select options) and the base's other tables. Pick the table by name or id; without one, the base's first table is read. Get base ids from list_bases.

### How do I automatically list Airtable records on airtable.com?

Ask an AI agent connected to Reduck to run reduck/airtable.com/list_records, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/airtable.com/list_records

### Is there a airtable.com API to list Airtable records?

You do not need one. "List Airtable records" drives the real airtable.com pages in a browser, so it works whether or not airtable.com offers an API for this.

### What information do I need to provide?

Required: baseId. Optional: table, maxRecords.

### What does it return?

It returns base, table, total, fields, tables, records, truncated.

### Do I need to be logged in to airtable.com?

Yes. It acts as you on airtable.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the airtable.com cookies saved by the Reduck extension.

### Does it change anything on airtable.com, or only read data?

It only reads. It looks things up on airtable.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/airtable.com/list_records, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/airtable.com/list_records

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/airtable.com/list_records
