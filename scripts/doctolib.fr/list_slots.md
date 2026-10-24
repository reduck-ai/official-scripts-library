# List Doctolib slots

Automatically list Doctolib slots on doctolib.fr. List a Doctolib practitioner's bookable appointment slots for one visit motive over a window of up to 15 days (Doctolib's limit); for a longer span, call again with a later start_date. Returns name, motive, bookable, availabilities (slots by day), total, next_slot (the next slot after an empty window), visit_motives, and booking_url. A motive name that matches several motives, an unknown motive id or an unknown profile fails with a message saying what to pass; pass motive_id to target one motive exactly. booking_url only opens the booking funnel; there is no per-slot link.

- Site: doctolib.fr
- Address: `reduck/doctolib.fr/list_slots`
- Updated: 2026-10-22 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/doctolib.fr/list_slots`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/doctolib.fr/list_slots
```

## Input

- `profile_path` (string, required): Relative path (with ?pid=practice-N) or full profile URL from search_practitioners.profile_path.
- `days` (integer, optional): Number of days to read from start_date, 1 to 15 (Doctolib serves at most 15 days at once). For a longer span, call again with start_date moved forward by days. Default 14.
- `motive` (string, optional): Visit-motive name substring (case-insensitive), e.g. 'première consultation', 'vidéo'. It must match exactly one of the practitioner's motives; when it matches several, the run fails and lists their ids, so pass motive_id. If omitted (and no motive_id), the first motive in Doctolib's order is used.
- `motive_id` (integer, optional): Exact visit-motive id (from search_practitioners.matched_visit_motive.id or this script's visit_motives). Takes precedence over motive; the deterministic way to target one of several same-named motives.
- `start_date` (string, optional): Optional ISO date YYYY-MM-DD where the window starts. Defaults to today (UTC). Use it to page through later windows.

## Output

- `bookable` (boolean, required)
- `booking_url` (string, required): Entry point to Doctolib's booking funnel (motive/slot selection happens in-app; no per-slot deep link exists).
- `profile_path` (string, required)
- `visit_motives` (array, required)
- `availabilities` (array, required): Days with at least one slot. Empty if none in window (see next_slot).
- `name` (string | null, optional)
- `total` (integer | null, optional): Total slots in the scanned window.
- `motive` (object | null, optional)
- `next_slot` (string | object | null, optional): Next availability beyond the window when the window is empty; null when slots exist.

## FAQ

### What does "List Doctolib slots" do?

List a Doctolib practitioner's bookable appointment slots for one visit motive over a window of up to 15 days (Doctolib's limit); for a longer span, call again with a later start_date. Returns name, motive, bookable, availabilities (slots by day), total, next_slot (the next slot after an empty window), visit_motives, and booking_url. A motive name that matches several motives, an unknown motive id or an unknown profile fails with a message saying what to pass; pass motive_id to target one motive exactly. booking_url only opens the booking funnel; there is no per-slot link.

### How do I automatically list Doctolib slots on doctolib.fr?

Ask an AI agent connected to Reduck to run reduck/doctolib.fr/list_slots, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/doctolib.fr/list_slots

### Is there a doctolib.fr API to list Doctolib slots?

You do not need one. "List Doctolib slots" drives the real doctolib.fr pages in a browser, so it works whether or not doctolib.fr offers an API for this.

### What information do I need to provide?

Required: profile_path. Optional: days, motive, motive_id, start_date.

### What does it return?

It returns name, total, motive, bookable, next_slot, booking_url, profile_path, visit_motives, availabilities.

### Do I need to be logged in to doctolib.fr?

No. It only uses pages of doctolib.fr that are reachable without signing in.

### Does it change anything on doctolib.fr, or only read data?

Unknown: its author has not declared whether it changes anything on doctolib.fr, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/doctolib.fr/list_slots, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/doctolib.fr/list_slots

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/doctolib.fr/list_slots
