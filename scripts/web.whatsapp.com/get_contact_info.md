# WhatsApp — Get contact info

Automatically get contact info on web.whatsapp.com. Open a chat by exact name and read its Contact-info panel: phone number, About text, shared media/links/docs count, and number of groups in common. For a 1:1 contact (for groups, use get_group_members). If the browser isn't linked to WhatsApp, it says so straight away instead of waiting for a chat list that will never load.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/get_contact_info`
- Updated: 2026-09-03 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/get_contact_info`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_contact_info
```

## Input

- `name` (string, required): Exact contact/chat name to open (the `name` field from get_inbox).

## Output

- `name` (string | null, required)
- `about` (string | null, required): About text; null if empty.
- `phone` (string | null, required): Phone number / subtitle under the name.
- `mediaCount` (integer | null, required): Shared media/links/docs count; null if block absent.
- `groupsInCommon` (integer, required)

## FAQ

### What does "WhatsApp — Get contact info" do?

Open a chat by exact name and read its Contact-info panel: phone number, About text, shared media/links/docs count, and number of groups in common. For a 1:1 contact (for groups, use get_group_members). If the browser isn't linked to WhatsApp, it says so straight away instead of waiting for a chat list that will never load.

### How do I automatically get contact info on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/get_contact_info, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_contact_info

### Is there a web.whatsapp.com API to get contact info?

You do not need one. "WhatsApp — Get contact info" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: name.

### What does it return?

It returns name, about, phone, mediaCount, groupsInCommon.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It only reads. It looks things up on web.whatsapp.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/get_contact_info, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_contact_info

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/get_contact_info
