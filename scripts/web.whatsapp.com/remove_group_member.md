# WhatsApp — Remove group member

Automatically remove group member on web.whatsapp.com. Remove a member from a WhatsApp group by exact names. Admin-only; removal notifies the whole group and cannot be undone from here, so confirm the exact group and member name with the user before running.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/remove_group_member`
- Updated: 2026-08-27 (v11)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/remove_group_member`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/remove_group_member
```

## Input

- `group` (string, required)
- `member` (string, required)

## Output

- `group` (string, required)
- `member` (string, required)
- `removed` (boolean, required)

## FAQ

### What does "WhatsApp — Remove group member" do?

Remove a member from a WhatsApp group by exact names. Admin-only; removal notifies the whole group and cannot be undone from here, so confirm the exact group and member name with the user before running.

### How do I automatically remove group member on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/remove_group_member, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/remove_group_member

### Is there a web.whatsapp.com API to remove group member?

You do not need one. "WhatsApp — Remove group member" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: group, member.

### What does it return?

It returns group, member, removed.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It makes changes on web.whatsapp.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/remove_group_member, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/remove_group_member

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/remove_group_member
