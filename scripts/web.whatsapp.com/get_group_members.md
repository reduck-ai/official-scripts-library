# WhatsApp — Get group members

Automatically get group members on web.whatsapp.com. Open a group by its exact name and list its participants (name and admin status). Small groups read from the inline list; large groups expand via "View all" and scroll the full member modal. Returns the group name, total member count, and the members.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/get_group_members`
- Updated: 2026-09-03 (v11)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/get_group_members`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_group_members
```

## Input

- `name` (string, required): Exact group name to open (the `name` field from get_inbox).

## Output

- `group` (string | null, required): Group name.
- `members` (array, required)
- `memberCount` (integer, required): Total members actually retrieved (equal to members.length).

## FAQ

### What does "WhatsApp — Get group members" do?

Open a group by its exact name and list its participants (name and admin status). Small groups read from the inline list; large groups expand via "View all" and scroll the full member modal. Returns the group name, total member count, and the members.

### How do I automatically get group members on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/get_group_members, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_group_members

### Is there a web.whatsapp.com API to get group members?

You do not need one. "WhatsApp — Get group members" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: name.

### What does it return?

It returns group, members, memberCount.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It only reads. It looks things up on web.whatsapp.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/get_group_members, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_group_members

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/get_group_members
