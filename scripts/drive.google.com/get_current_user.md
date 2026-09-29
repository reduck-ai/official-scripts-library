# Get Current Drive User

Automatically get Current Drive User on drive.google.com. Report which Google account Google Drive is signed in as in this browser: display name and email, read from Google's account button. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Drive scripts.

- Site: drive.google.com
- Address: `reduck/drive.google.com/get_current_user`
- Updated: 2026-09-28 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/drive.google.com/get_current_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/drive.google.com/get_current_user
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional)

## FAQ

### What does "Get Current Drive User" do?

Report which Google account Google Drive is signed in as in this browser: display name and email, read from Google's account button. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Drive scripts.

### How do I automatically get Current Drive User on drive.google.com?

Ask an AI agent connected to Reduck to run reduck/drive.google.com/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drive.google.com/get_current_user

### Is there a drive.google.com API to get Current Drive User?

You do not need one. "Get Current Drive User" drives the real drive.google.com pages in a browser, so it works whether or not drive.google.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email, loggedIn.

### Do I need to be logged in to drive.google.com?

Yes. It acts as you on drive.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the drive.google.com cookies saved by the Reduck extension.

### Does it change anything on drive.google.com, or only read data?

It only reads. It looks things up on drive.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/drive.google.com/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drive.google.com/get_current_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/drive.google.com/get_current_user
