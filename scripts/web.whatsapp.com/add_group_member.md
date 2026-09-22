# WhatsApp — Add group member

Automatically add group member on web.whatsapp.com. Add a contact to an existing WhatsApp group, both named exactly. Confirms afterwards that the contact really appears in the group, and reports clearly if they were already a member. You must be an admin of the group, and the group is notified when someone is added.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/add_group_member`
- Updated: 2026-08-27 (v12)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/add_group_member`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/add_group_member
```

## Input

- `group` (string, required): Exact group name
- `member` (string, required): Exact contact name to add

## Output

- `added` (boolean, required)
- `group` (string, required)
- `member` (string, required)

## FAQ

### What does "WhatsApp — Add group member" do?

Add a contact to an existing WhatsApp group, both named exactly. Confirms afterwards that the contact really appears in the group, and reports clearly if they were already a member. You must be an admin of the group, and the group is notified when someone is added.

### How do I automatically add group member on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/add_group_member, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/add_group_member

### Is there a web.whatsapp.com API to add group member?

You do not need one. "WhatsApp — Add group member" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: group, member.

### What does it return?

It returns added, group, member.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It makes changes on web.whatsapp.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/add_group_member, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/add_group_member

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/add_group_member
