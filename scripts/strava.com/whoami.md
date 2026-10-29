# Get the signed-in Strava athlete

Automatically get the signed-in Strava athlete on strava.com. Returns the Strava athlete this browser is signed in as: id, display name, subscriber status and profile photo. Fails with a sign-in message when no one is signed in.

- Site: strava.com
- Address: `reduck/strava.com/whoami`
- Updated: 2026-10-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/strava.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/strava.com/whoami
```

## Input

It takes no input.

## Output

- `athlete_id` (string, required)
- `name` (string | null, optional)
- `premium` (boolean, optional)
- `photo_url` (string | null, optional)
- `profile_url` (string, optional)

## FAQ

### What does "Get the signed-in Strava athlete" do?

Returns the Strava athlete this browser is signed in as: id, display name, subscriber status and profile photo. Fails with a sign-in message when no one is signed in.

### How do I automatically get the signed-in Strava athlete on strava.com?

Ask an AI agent connected to Reduck to run reduck/strava.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/strava.com/whoami

### Is there a strava.com API to get the signed-in Strava athlete?

You do not need one. "Get the signed-in Strava athlete" drives the real strava.com pages in a browser, so it works whether or not strava.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, premium, photo_url, athlete_id, profile_url.

### Do I need to be logged in to strava.com?

Yes. It acts as you on strava.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the strava.com cookies saved by the Reduck extension.

### Does it change anything on strava.com, or only read data?

It only reads. It looks things up on strava.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/strava.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/strava.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/strava.com/whoami
