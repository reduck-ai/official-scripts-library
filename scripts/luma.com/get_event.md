# Get Luma event details

Automatically get Luma event details on luma.com. Get the full public details of a Luma event by its slug: description, categories, hosts (with social handles), venue, and guest/ticket counts.

- Site: luma.com
- Address: `reduck/luma.com/get_event`
- Updated: 2026-09-25 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/luma.com/get_event`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/luma.com/get_event
```

## Input

- `slug` (string, required): The event's short Luma slug, e.g. "9n5kxo7k" from luma.com/9n5kxo7k.

## Output

- `name` (string, required)
- `slug` (string, required)
- `event_id` (string, required)
- `start_at` (string, required)
- `city` (string | null, optional)
- `hosts` (array, optional)
- `end_at` (string | null, optional)
- `is_free` (boolean | null, optional): Whether every ticket is free.
- `timezone` (string | null, optional)
- `cover_url` (string | null, optional)
- `categories` (array, optional)
- `coordinate` (object | null, optional)
- `venue_name` (string | null, optional)
- `description` (string | null, optional)
- `guest_count` (integer | null, optional): As Luma reports it. Luma reports 0 when the organizer hides the guest list (show_guest_list false), whatever the real count.
- `full_address` (string | null, optional)
- `ticket_count` (integer | null, optional)
- `calendar_name` (string | null, optional)
- `calendar_slug` (string | null, optional)
- `location_type` (string | null, optional)
- `show_guest_list` (boolean | null, optional): Whether the organizer shows the guest list to guests. False: get_event_attendees returns only the public preview, even after registering.
- `require_approval` (boolean | null, optional): Whether a registration waits for the organizer's approval.
- `registration_questions` (array, optional): The event's registration form as Luma declares it, in order. `id` is a key register_to_event's `answers` takes.
- `registration_availability` (string | null, optional)

## FAQ

### What does "Get Luma event details" do?

Get the full public details of a Luma event by its slug: description, categories, hosts (with social handles), venue, and guest/ticket counts.

### How do I automatically get Luma event details on luma.com?

Ask an AI agent connected to Reduck to run reduck/luma.com/get_event, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/luma.com/get_event

### Is there a luma.com API to get Luma event details?

You do not need one. "Get Luma event details" drives the real luma.com pages in a browser, so it works whether or not luma.com offers an API for this.

### What information do I need to provide?

Required: slug.

### What does it return?

It returns city, name, slug, hosts, end_at, is_free, event_id, start_at, timezone, cover_url, categories, coordinate, venue_name, description, guest_count, full_address, ticket_count, calendar_name, calendar_slug, location_type, show_guest_list, require_approval, registration_questions, registration_availability.

### Do I need to be logged in to luma.com?

No. It only uses pages of luma.com that are reachable without signing in.

### Does it change anything on luma.com, or only read data?

It only reads. It looks things up on luma.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/luma.com/get_event, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/luma.com/get_event

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/luma.com/get_event
