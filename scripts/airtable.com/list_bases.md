# List Airtable bases

Automatically list Airtable bases on airtable.com. List the Airtable bases the signed-in account can open, grouped by workspace, with each base's id, link and your access level. Pass a base id to list_records to read its tables and records.

- Site: airtable.com
- Address: `reduck/airtable.com/list_bases`
- Updated: 2026-11-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/airtable.com/list_bases`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/airtable.com/list_bases
```

## Input

It takes no input.

## Output

- `account` (string | null, required): Id of the signed-in Airtable user.
- `workspaces` (array, required)

## FAQ

### What does "List Airtable bases" do?

List the Airtable bases the signed-in account can open, grouped by workspace, with each base's id, link and your access level. Pass a base id to list_records to read its tables and records.

### How do I automatically list Airtable bases on airtable.com?

Ask an AI agent connected to Reduck to run reduck/airtable.com/list_bases, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/airtable.com/list_bases

### Is there a airtable.com API to list Airtable bases?

You do not need one. "List Airtable bases" drives the real airtable.com pages in a browser, so it works whether or not airtable.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns account, workspaces.

### Do I need to be logged in to airtable.com?

Yes. It acts as you on airtable.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the airtable.com cookies saved by the Reduck extension.

### Does it change anything on airtable.com, or only read data?

It only reads. It looks things up on airtable.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/airtable.com/list_bases, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/airtable.com/list_bases

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/airtable.com/list_bases
