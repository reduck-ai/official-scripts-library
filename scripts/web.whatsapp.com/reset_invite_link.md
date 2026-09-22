# WhatsApp — Reset group invite link

Automatically reset group invite link on web.whatsapp.com. Reset (revoke + regenerate) a WhatsApp group's invite link by exact name. The old link stops working immediately. Admin-only. Returns the group name plus the old and new invite links.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/reset_invite_link`
- Updated: 2026-08-26 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/reset_invite_link`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/reset_invite_link
```

## Input

- `name` (string, required): Group name, matched exactly against the group's display name. You must be an admin of the group to reset its invite link.

## Output

- `group` (string, required)
- `newLink` (string, required): The invite link after the reset. Any previously shared link stops working.
- `oldLink` (string, required): The invite link as it was before the reset.

## FAQ

### What does "WhatsApp — Reset group invite link" do?

Reset (revoke + regenerate) a WhatsApp group's invite link by exact name. The old link stops working immediately. Admin-only. Returns the group name plus the old and new invite links.

### How do I automatically reset group invite link on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/reset_invite_link, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/reset_invite_link

### Is there a web.whatsapp.com API to reset group invite link?

You do not need one. "WhatsApp — Reset group invite link" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: name.

### What does it return?

It returns group, newLink, oldLink.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It makes changes on web.whatsapp.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/reset_invite_link, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/reset_invite_link

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/reset_invite_link
