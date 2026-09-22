# WhatsApp — Rename group

Automatically rename group on web.whatsapp.com. Rename a WhatsApp group: open by exact current name → group-info drawer → edit subject → save. Verifies the new subject. Admin-only. Notifies the group.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/rename_group`
- Updated: 2026-08-04 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/rename_group`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/rename_group
```

## Input

- `name` (string, required): Exact current group name
- `newName` (string, required): New group subject

## Output

- `name` (string, required)
- `newName` (string, required)
- `renamed` (boolean, required)

## FAQ

### What does "WhatsApp — Rename group" do?

Rename a WhatsApp group: open by exact current name → group-info drawer → edit subject → save. Verifies the new subject. Admin-only. Notifies the group.

### How do I automatically rename group on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/rename_group, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/rename_group

### Is there a web.whatsapp.com API to rename group?

You do not need one. "WhatsApp — Rename group" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: name, newName.

### What does it return?

It returns name, newName, renamed.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It makes changes on web.whatsapp.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/rename_group, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/rename_group

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/rename_group
