# List my Strava activities

Automatically list my Strava activities on strava.com. Lists the signed-in athlete's own Strava activities, 20 per page: id, name, sport, start time, distance, moving and elapsed time, elevation gain, and whether it is private, a commute or on a trainer. Filter by title keywords, sport, workout tags, private only or trainer only, and sort by date, title, time, distance, elevation or relative effort; the gear filter is not offered. Distances are in meters, times in seconds. An account or filter with no activities returns an empty list. Pass page to read further; total and has_more say how many there are.

- Site: strava.com
- Address: `reduck/strava.com/list_activities`
- Updated: 2026-10-28 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/strava.com/list_activities`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/strava.com/list_activities
```

## Input

- `page` (integer, optional)
- `order` (string | null, optional): null keeps the site's order, newest first.
- `keywords` (string, optional): Words to match in activity titles.
- `sport_type` (string | null, optional)
- `private_only` (boolean, optional)
- `trainer_only` (boolean, optional)
- `workout_tags` (array, optional): Workout tags, any of: 0 long run, 1 race, 2 workout, 3 commute, 12 recovery, 13 with pet, 14 for a cause, 15 competition, 16 with kid.

## Output

- `page` (integer, required)
- `total` (integer | null, required)
- `activities` (array, required)
- `has_more` (boolean, optional)

## FAQ

### What does "List my Strava activities" do?

Lists the signed-in athlete's own Strava activities, 20 per page: id, name, sport, start time, distance, moving and elapsed time, elevation gain, and whether it is private, a commute or on a trainer. Filter by title keywords, sport, workout tags, private only or trainer only, and sort by date, title, time, distance, elevation or relative effort; the gear filter is not offered. Distances are in meters, times in seconds. An account or filter with no activities returns an empty list. Pass page to read further; total and has_more say how many there are.

### How do I automatically list my Strava activities on strava.com?

Ask an AI agent connected to Reduck to run reduck/strava.com/list_activities, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/strava.com/list_activities

### Is there a strava.com API to list my Strava activities?

You do not need one. "List my Strava activities" drives the real strava.com pages in a browser, so it works whether or not strava.com offers an API for this.

### What information do I need to provide?

Optional: page, order, keywords, sport_type, private_only, trainer_only, workout_tags.

### What does it return?

It returns page, total, has_more, activities.

### Do I need to be logged in to strava.com?

Yes. It acts as you on strava.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the strava.com cookies saved by the Reduck extension.

### Does it change anything on strava.com, or only read data?

It only reads. It looks things up on strava.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/strava.com/list_activities, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/strava.com/list_activities

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/strava.com/list_activities
