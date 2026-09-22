# List Attio records

Automatically list Attio records on attio.com. List records from an Attio object list view (e.g. "companies" or "people"), reading whatever columns the current default view shows. Returns each record's name and its visible column values as a flat key/value map.

- Site: attio.com
- Address: `reduck/attio.com/list_records`
- Updated: 2026-09-04 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/attio.com/list_records`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/attio.com/list_records
```

## Input

- `object` (string, required): Object slug, e.g. "companies" or "people"
- `workspace` (string, required): Attio workspace slug — the segment right after app.attio.com/ in the URL, e.g. "acme"

## Output

- `object` (string, required)
- `records` (array, required)

## FAQ

### What does "List Attio records" do?

List records from an Attio object list view (e.g. "companies" or "people"), reading whatever columns the current default view shows. Returns each record's name and its visible column values as a flat key/value map.

### How do I automatically list Attio records on attio.com?

Ask an AI agent connected to Reduck to run reduck/attio.com/list_records, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/attio.com/list_records

### Is there a attio.com API to list Attio records?

You do not need one. "List Attio records" drives the real attio.com pages in a browser, so it works whether or not attio.com offers an API for this.

### What information do I need to provide?

Required: workspace, object.

### What does it return?

It returns object, records.

### Do I need to be logged in to attio.com?

Yes. It acts as you on attio.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the attio.com cookies saved by the Reduck extension.

### Does it change anything on attio.com, or only read data?

It only reads. It looks things up on attio.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/attio.com/list_records, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/attio.com/list_records

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/attio.com/list_records
