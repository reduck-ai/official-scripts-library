# Get Luma event attendees

Automatically get Luma event attendees on luma.com. An unofficial Luma API: get the attendees of a Luma event programmatically, from code or from an AI agent, with typed JSON in and out. Luma's official API only returns guests of events you host.

- Site: luma.com
- Address: `reduck/luma.com/get_event_attendees`
- Updated: 2026-09-16 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/luma.com/get_event_attendees`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/luma.com/get_event_attendees
```

## Input

- `slug` (string, required): The event's short Luma slug, e.g. "9n5kxo7k" from luma.com/9n5kxo7k.
- `max_attendees` (integer, optional): Stop after roughly this many attendees instead of walking the whole roster. Omit to fetch everyone; large events run to several hundred.

## Output

- `slug` (string, required)
- `event_id` (string, required)
- `attendees` (array, required)
- `guest_count` (integer, required)
- `roster_scope` (string, required): "full" = every attendee Luma will disclose; "public_preview" = only the featured subset shown on the event page.
- `show_guest_list` (boolean, required)
- `roster_note` (string | null, optional): When roster_scope is public_preview, why the full roster was not available.
- `my_approval_status` (string | null, optional)

## FAQ

### What does "Get Luma event attendees" do?

Get the attendees of a Luma event. When the signed-in account is an approved guest and the organizer has the guest list switched on, this returns the FULL roster — every guest, paginated, with their public profile and social handles. Otherwise it falls back to the featured preview Luma shows on the event page and says why in roster_note, so \"few attendees\" is never mistaken for \"the event is empty\". Check roster_scope to tell the two apart. Returns public profile fields only — no email addresses — but it is still a list of real people, so treat the output as personal data.

### How do I automatically get Luma event attendees on luma.com?

Ask an AI agent connected to Reduck to run reduck/luma.com/get_event_attendees, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/luma.com/get_event_attendees

### Is there a luma.com API to get Luma event attendees?

You do not need one. "Get Luma event attendees" drives the real luma.com pages in a browser, so it works whether or not luma.com offers an API for this.

### What information do I need to provide?

Required: slug. Optional: max_attendees.

### What does it return?

It returns slug, event_id, attendees, guest_count, roster_note, roster_scope, show_guest_list, my_approval_status.

### Do I need to be logged in to luma.com?

Yes. It acts as you on luma.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the luma.com cookies saved by the Reduck extension.

### Does it change anything on luma.com, or only read data?

It only reads. It looks things up on luma.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/luma.com/get_event_attendees, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/luma.com/get_event_attendees

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/luma.com/get_event_attendees
