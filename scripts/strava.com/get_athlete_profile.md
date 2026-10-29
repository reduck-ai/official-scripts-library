# Get a Strava athlete profile

Automatically get a Strava athlete profile on strava.com. Returns a Strava athlete's profile: name, photo, location, follower and following counts, club names, and the activities shown on the profile page. Counts are null when the profile hides them. Fails when the athlete does not exist.

- Site: strava.com
- Address: `reduck/strava.com/get_athlete_profile`
- Updated: 2026-10-28 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/strava.com/get_athlete_profile`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/strava.com/get_athlete_profile
```

## Input

- `athlete_id` (string, required): The number in an athlete URL, strava.com/athletes/<id>. Get your own from strava.com/whoami.

## Output

- `name` (string, required)
- `private` (boolean, required): True when the profile is only visible to followers: clubs and activities are then not shown.
- `athlete_id` (string, required)
- `clubs` (array, optional)
- `location` (string | null, optional)
- `followers` (integer | null, optional)
- `following` (integer | null, optional)
- `photo_url` (string | null, optional)
- `recent_activities` (array, optional)

## FAQ

### What does "Get a Strava athlete profile" do?

Returns a Strava athlete's profile: name, photo, location, follower and following counts, club names, and the activities shown on the profile page. Counts are null when the profile hides them. Fails when the athlete does not exist.

### How do I automatically get a Strava athlete profile on strava.com?

Ask an AI agent connected to Reduck to run reduck/strava.com/get_athlete_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/strava.com/get_athlete_profile

### Is there a strava.com API to get a Strava athlete profile?

You do not need one. "Get a Strava athlete profile" drives the real strava.com pages in a browser, so it works whether or not strava.com offers an API for this.

### What information do I need to provide?

Required: athlete_id.

### What does it return?

It returns name, clubs, private, location, followers, following, photo_url, athlete_id, recent_activities.

### Do I need to be logged in to strava.com?

Yes. It acts as you on strava.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the strava.com cookies saved by the Reduck extension.

### Does it change anything on strava.com, or only read data?

It only reads. It looks things up on strava.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/strava.com/get_athlete_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/strava.com/get_athlete_profile

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/strava.com/get_athlete_profile
