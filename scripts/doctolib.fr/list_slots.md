# List Doctolib slots

Automatically list Doctolib slots on doctolib.fr. List a Doctolib practitioner's bookable appointment slots over the next N days for a given visit motive. Returns name, motive, bookable, availabilities (slots by day), total, next_slot, visit_motives, and booking_url. A practitioner can expose several motives sharing one name across practices, so pass motive_id to target one exactly; booking_url only opens the funnel, there is no per-slot deep link.

- Site: doctolib.fr
- Address: `reduck/doctolib.fr/list_slots`
- Updated: 2026-08-05 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/doctolib.fr/list_slots`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/doctolib.fr/list_slots
```

## Input

- `profile_path` (string, required): Relative path (with ?pid=practice-N) or full profile URL from search_practitioners.profile_path.
- `days` (integer, optional): Number of days to scan from start_date. Default 14.
- `motive` (string, optional): Visit-motive name substring (case-insensitive), e.g. 'première consultation', 'vidéo'. If omitted, the first motive by display position is used. Note: a practitioner can expose several motives sharing one name (different practices/agendas) — pass motive_id to disambiguate exactly.
- `motive_id` (integer, optional): Exact visit-motive id (from search_practitioners.matched_visit_motive.id or this script's visit_motives). Takes precedence over motive; the deterministic way to target one of several same-named motives.
- `start_date` (string, optional): Optional ISO date YYYY-MM-DD lower bound. Defaults to now.

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

List a Doctolib practitioner's bookable appointment slots over the next N days for a given visit motive. Returns name, motive, bookable, availabilities (slots by day), total, next_slot, visit_motives, and booking_url. A practitioner can expose several motives sharing one name across practices, so pass motive_id to target one exactly; booking_url only opens the funnel, there is no per-slot deep link.

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
