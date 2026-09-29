# Get Current Calendar User

Automatically get Current Calendar User on calendar.google.com. Report which Google account Google Calendar is signed in as in this browser: display name and email, read from Google's account button. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Calendar scripts.

- Site: calendar.google.com
- Address: `reduck/calendar.google.com/get_current_user`
- Updated: 2026-09-28 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/calendar.google.com/get_current_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/get_current_user
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional)

## FAQ

### What does "Get Current Calendar User" do?

Report which Google account Google Calendar is signed in as in this browser: display name and email, read from Google's account button. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Calendar scripts.

### How do I automatically get Current Calendar User on calendar.google.com?

Ask an AI agent connected to Reduck to run reduck/calendar.google.com/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/get_current_user

### Is there a calendar.google.com API to get Current Calendar User?

You do not need one. "Get Current Calendar User" drives the real calendar.google.com pages in a browser, so it works whether or not calendar.google.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email, loggedIn.

### Do I need to be logged in to calendar.google.com?

Yes. It acts as you on calendar.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the calendar.google.com cookies saved by the Reduck extension.

### Does it change anything on calendar.google.com, or only read data?

It only reads. It looks things up on calendar.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/calendar.google.com/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/get_current_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/calendar.google.com/get_current_user
