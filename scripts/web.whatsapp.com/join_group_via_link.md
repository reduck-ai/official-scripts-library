# join_group_via_link

Join a WhatsApp group from an invite link (https://chat.whatsapp.com/<code>) or bare code. Navigates the in-app accept flow → confirms the Join group dialog. Verifies you're in (composer appears). Returns the group name. Throws if the link is invalid/expired or you're already a member (no Join dialog appears).

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/join_group_via_link`
- Updated: 2026-08-27 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/join_group_via_link`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/join_group_via_link
```

## Input

- `link` (string, required): Full invite link https://chat.whatsapp.com/<code> or just the <code>

## Output

- `group` (string, required)
- `joined` (boolean, required)

## FAQ

### What does "join_group_via_link" do?

Join a WhatsApp group from an invite link (https://chat.whatsapp.com/<code>) or bare code. Navigates the in-app accept flow → confirms the Join group dialog. Verifies you're in (composer appears). Returns the group name. Throws if the link is invalid/expired or you're already a member (no Join dialog appears).

### What information do I need to provide?

Required: link.

### What does it return?

It returns group, joined.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It makes changes on web.whatsapp.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/join_group_via_link, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/join_group_via_link

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/join_group_via_link
