# Get a Strava segment and its leaderboard

Automatically get a Strava segment and its leaderboard on strava.com. Returns a Strava segment's name, sport, location, distance, grade and elevation, its effort and athlete totals, the KOM, QOM and Local Legend holders, and one page (25 rows) of its leaderboard. The leaderboard can be everyone, your own efforts, people you follow, one age group or one weight class, filtered by gender and by today, this week, this month or this year; has_more says whether another page exists. Club leaderboards are not offered. Distances are in meters, times in seconds, speeds in meters per second. Fails when the segment does not exist or is private.

- Site: strava.com
- Address: `reduck/strava.com/get_segment`
- Updated: 2026-10-28 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/strava.com/get_segment`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/strava.com/get_segment
```

## Input

- `segment_id` (string, required): The number in a segment URL, strava.com/segments/<id>.
- `page` (integer, optional): Leaderboard page, 25 rows each.
- `filter` (string, optional): Which leaderboard to read: everyone, your own efforts, people you follow, one age group, or one weight class.
- `gender` (string, optional)
- `date_range` (string | null, optional): null is all time.
- `filter_value` (string | null, optional): Required for age_group: 20_24, 25_34, 35_44, 45_54, 55_64, 65_69, 70_74 or 75_plus (years). Required for weight_class: 0_54, 55_64, 65_74, 75_84, 85_94, 95_104, 105_114 or 115_plus (kg). Leave null for the other filters.

## Output

- `name` (string, required)
- `page` (integer, required)
- `segment_id` (string, required)
- `leaderboard` (array, required)
- `filter` (string, optional)
- `gender` (string, optional)
- `hazard` (boolean, optional)
- `has_more` (boolean, optional)
- `location` (string | null, optional)
- `verified` (boolean, optional)
- `date_range` (string | null, optional)
- `distance_m` (number | null, optional)
- `elev_low_m` (number | null, optional)
- `star_count` (integer | null, optional)
- `elev_gain_m` (number | null, optional)
- `elev_high_m` (number | null, optional)
- `top_efforts` (array, optional)
- `filter_value` (string | null, optional)
- `local_legend` (object | null, optional)
- `activity_type` (string | null, optional)
- `avg_grade_pct` (number | null, optional)
- `total_efforts` (integer | null, optional)
- `climb_category` (string | null, optional)
- `total_athletes` (integer | null, optional)
- `my_effort_count` (integer | null, optional)
- `leaderboard_total` (integer | null, optional)

## FAQ

### What does "Get a Strava segment and its leaderboard" do?

Returns a Strava segment's name, sport, location, distance, grade and elevation, its effort and athlete totals, the KOM, QOM and Local Legend holders, and one page (25 rows) of its leaderboard. The leaderboard can be everyone, your own efforts, people you follow, one age group or one weight class, filtered by gender and by today, this week, this month or this year; has_more says whether another page exists. Club leaderboards are not offered. Distances are in meters, times in seconds, speeds in meters per second. Fails when the segment does not exist or is private.

### How do I automatically get a Strava segment and its leaderboard on strava.com?

Ask an AI agent connected to Reduck to run reduck/strava.com/get_segment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/strava.com/get_segment

### Is there a strava.com API to get a Strava segment and its leaderboard?

You do not need one. "Get a Strava segment and its leaderboard" drives the real strava.com pages in a browser, so it works whether or not strava.com offers an API for this.

### What information do I need to provide?

Required: segment_id. Optional: page, filter, gender, date_range, filter_value.

### What does it return?

It returns name, page, filter, gender, hazard, has_more, location, verified, date_range, distance_m, elev_low_m, segment_id, star_count, elev_gain_m, elev_high_m, leaderboard, top_efforts, filter_value, local_legend, activity_type, avg_grade_pct, total_efforts, climb_category, total_athletes, my_effort_count, leaderboard_total.

### Do I need to be logged in to strava.com?

Yes. It acts as you on strava.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the strava.com cookies saved by the Reduck extension.

### Does it change anything on strava.com, or only read data?

It only reads. It looks things up on strava.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/strava.com/get_segment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/strava.com/get_segment

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/strava.com/get_segment
