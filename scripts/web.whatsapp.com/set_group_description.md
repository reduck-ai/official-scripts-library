# WhatsApp — Set group description

Automatically set group description on web.whatsapp.com. Set/replace a WhatsApp group's description by exact group name. Notifies the group's members.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/set_group_description`
- Updated: 2026-08-27 (v10)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/set_group_description`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/set_group_description
```

## Input

- `name` (string, required): Exact group name
- `description` (string, required): Group description text. A long description is stored in full, but WhatsApp only renders its first ~100 characters in the group-info panel.

## Output

- `set` (boolean, required)
- `name` (string, required)
- `description` (string, required)

## FAQ

### What does "WhatsApp — Set group description" do?

Set/replace a WhatsApp group's description by exact group name. Notifies the group's members.

### How do I automatically set group description on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/set_group_description, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/set_group_description

### Is there a web.whatsapp.com API to set group description?

You do not need one. "WhatsApp — Set group description" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: name, description.

### What does it return?

It returns set, name, description.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It makes changes on web.whatsapp.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/set_group_description, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/set_group_description

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/set_group_description
