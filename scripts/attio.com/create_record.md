# Create Attio record

Automatically create Attio record on attio.com. Create a new record (e.g. a Company or a Person) in Attio via the object's "New <Type>" quick-create form, setting the record's Name field. Returns the new record's id and detail-page URL.

- Site: attio.com
- Address: `reduck/attio.com/create_record`
- Updated: 2026-09-01 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/attio.com/create_record`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/attio.com/create_record
```

## Input

- `name` (string, required): Value to set in the record's Name field
- `object` (string, required): Object slug for the list URL, e.g. "companies" or "people"
- `workspace` (string, required): Attio workspace slug, e.g. "reduck"
- `record_type_label` (string, required): Singular label as it appears on the "New <Type>" button, e.g. "Company" or "Person"

## Output

- `url` (string, required)
- `name` (string, required)
- `id` (string | null, optional)

## FAQ

### What does "Create Attio record" do?

Create a new record (e.g. a Company or a Person) in Attio via the object's "New <Type>" quick-create form, setting the record's Name field. Returns the new record's id and detail-page URL.

### How do I automatically create Attio record on attio.com?

Ask an AI agent connected to Reduck to run reduck/attio.com/create_record, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/attio.com/create_record

### Is there a attio.com API to create Attio record?

You do not need one. "Create Attio record" drives the real attio.com pages in a browser, so it works whether or not attio.com offers an API for this.

### What information do I need to provide?

Required: workspace, object, record_type_label, name.

### What does it return?

It returns id, url, name.

### Do I need to be logged in to attio.com?

Yes. It acts as you on attio.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the attio.com cookies saved by the Reduck extension.

### Does it change anything on attio.com, or only read data?

It makes changes on attio.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/attio.com/create_record, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/attio.com/create_record

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/attio.com/create_record
