# WhatsApp — Get group invite link

Automatically get group invite link on web.whatsapp.com. Get the shareable invite link (https://chat.whatsapp.com/...) of a WhatsApp group by exact name. Opens the group-info drawer → Invite to group via link → reads the displayed link. Admin-only (non-admins can't see the link). Returns the group name and the invite URL.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/get_group_invite_link`
- Updated: 2026-09-03 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/get_group_invite_link`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_group_invite_link
```

## Input

- `name` (string, required): Group name, matched exactly against the group's display name

## Output

- `link` (string, required): https://chat.whatsapp.com/<code>
- `group` (string, required)

## FAQ

### What does "WhatsApp — Get group invite link" do?

Get the shareable invite link (https://chat.whatsapp.com/...) of a WhatsApp group by exact name. Opens the group-info drawer → Invite to group via link → reads the displayed link. Admin-only (non-admins can't see the link). Returns the group name and the invite URL.

### How do I automatically get group invite link on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/get_group_invite_link, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_group_invite_link

### Is there a web.whatsapp.com API to get group invite link?

You do not need one. "WhatsApp — Get group invite link" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: name.

### What does it return?

It returns link, group.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It only reads. It looks things up on web.whatsapp.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/get_group_invite_link, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_group_invite_link

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/get_group_invite_link
