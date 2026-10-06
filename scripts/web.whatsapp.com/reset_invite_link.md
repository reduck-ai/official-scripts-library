# WhatsApp — Reset group invite link

Automatically reset group invite link on web.whatsapp.com. Revokes a group's current join link and returns both the old URL and the newly generated one.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/reset_invite_link`
- Updated: 2026-10-05 (v6)
- Author: Reduck AI (reduck)

## About

By hand, an admin opens the group info, taps Invite via link, then Reset link and confirms. This does the same in WhatsApp Web, which helps when you look after several groups or want an agent to handle it on request. Pass the group's exact display name, for example "Sunday Long Run 10k", and you get back group, oldLink and newLink. The old chat.whatsapp.com URL stops working once the reset goes through and WhatsApp offers no undo, so oldLink is only a record of what to search for and replace in posts and bios. The run waits until the link shown in the panel actually changes before it returns, and it clicks nothing further if the confirmation dialog does not hold the expected two buttons. You must be an admin of the group and have WhatsApp Web linked in the browser. Each run handles one group.

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

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "group": "…",
  "newLink": "…",
  "oldLink": "…"
}
```

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

It makes changes on web.whatsapp.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/reset_invite_link, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/reset_invite_link

### Who maintains it?

It is part of Reduck's official curated catalogue.

### What does "invite link was reset" mean on WhatsApp?

A group admin replaced the group's join link, so the URL or QR code you were given no longer works. Ask someone in the group for the current link, or ask an admin to add you directly.

### Does resetting the invite link remove anyone from the group?

No. The run opens the invite panel, resets the link and stops without touching the member list. If a spammer already got in, remove them separately, for instance with get_group_members to find them and remove_group_member to take them out.

### What happens if two of my WhatsApp groups have the same name?

The name must match the chat title exactly, emoji and capitals included. If two groups share it, the reset hits whichever matching row the script finds first, and you cannot choose which. Since the reset cannot be undone, give one group a unique name in the WhatsApp app first, where you can see which group you have open, then run this with that name.

### What error do I get if I am not an admin of the group?

The invite-link row never appears in the group info panel, so the run fails with a message saying no invite-link row was found and that only an admin can reset the link. Nothing is changed in that case.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/reset_invite_link
