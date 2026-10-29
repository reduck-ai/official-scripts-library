# Get a Strava activity

Automatically get a Strava activity on strava.com. Returns one Strava activity: name, description, sport, local start time, location, distance, moving time, elevation gain, power and energy when recorded, the athlete, kudos and comment counts, and its segment efforts. Distances are in meters, times in seconds. The start time is null for activities whose page does not carry it as data (runs, for example), and shows 00:00:01 when the athlete hides start times. Fails when the activity does not exist or this account cannot see it.

- Site: strava.com
- Address: `reduck/strava.com/get_activity`
- Updated: 2026-10-28 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/strava.com/get_activity`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/strava.com/get_activity
```

## Input

- `activity_id` (string, required): The number in an activity URL, strava.com/activities/<id>.

## Output

- `name` (string, required)
- `activity_id` (string, required)
- `date` (string | null, optional): Local start time, ISO 8601 without zone.
- `type` (string | null, optional)
- `trainer` (boolean | null, optional)
- `location` (string | null, optional)
- `avg_watts` (number | null, optional)
- `athlete_id` (string | null, optional)
- `distance_m` (number | null, optional)
- `kilojoules` (number | null, optional)
- `description` (string | null, optional)
- `elev_gain_m` (number | null, optional)
- `kudos_count` (integer | null, optional)
- `athlete_name` (string | null, optional)
- `moving_time_s` (number | null, optional)
- `comments_count` (integer | null, optional)
- `segment_efforts` (array, optional)

## FAQ

### What does "Get a Strava activity" do?

Returns one Strava activity: name, description, sport, local start time, location, distance, moving time, elevation gain, power and energy when recorded, the athlete, kudos and comment counts, and its segment efforts. Distances are in meters, times in seconds. The start time is null for activities whose page does not carry it as data (runs, for example), and shows 00:00:01 when the athlete hides start times. Fails when the activity does not exist or this account cannot see it.

### How do I automatically get a Strava activity on strava.com?

Ask an AI agent connected to Reduck to run reduck/strava.com/get_activity, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/strava.com/get_activity

### Is there a strava.com API to get a Strava activity?

You do not need one. "Get a Strava activity" drives the real strava.com pages in a browser, so it works whether or not strava.com offers an API for this.

### What information do I need to provide?

Required: activity_id.

### What does it return?

It returns date, name, type, trainer, location, avg_watts, athlete_id, distance_m, kilojoules, activity_id, description, elev_gain_m, kudos_count, athlete_name, moving_time_s, comments_count, segment_efforts.

### Do I need to be logged in to strava.com?

Yes. It acts as you on strava.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the strava.com cookies saved by the Reduck extension.

### Does it change anything on strava.com, or only read data?

It only reads. It looks things up on strava.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/strava.com/get_activity, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/strava.com/get_activity

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/strava.com/get_activity
