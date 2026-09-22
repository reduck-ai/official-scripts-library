# WhatsApp — Promote group admin

Automatically promote group admin on web.whatsapp.com. Promote a WhatsApp group member to admin by exact names. Notifies the group. You must be an admin yourself. Fails immediately with a clear error if the member is already an admin.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/promote_admin`
- Updated: 2026-08-24 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/promote_admin`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/promote_admin
```

## Input

- `group` (string, required): Exact group name
- `member` (string, required): Exact member name to promote

## Output

- `group` (string, required)
- `member` (string, required)
- `promoted` (boolean, required)

## FAQ

### What does "WhatsApp — Promote group admin" do?

Promote a WhatsApp group member to admin by exact names. Notifies the group. You must be an admin yourself. Fails immediately with a clear error if the member is already an admin.

### How do I automatically promote group admin on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/promote_admin, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/promote_admin

### Is there a web.whatsapp.com API to promote group admin?

You do not need one. "WhatsApp — Promote group admin" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: group, member.

### What does it return?

It returns group, member, promoted.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It makes changes on web.whatsapp.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/promote_admin, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/promote_admin

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/promote_admin
