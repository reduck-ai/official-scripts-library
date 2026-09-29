# Get Current User

Automatically get Current User on crunchbase.com. Report which Crunchbase account this browser is signed in as: email, first name and last name from Account Settings > Your Info. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Crunchbase scripts.

- Site: crunchbase.com
- Address: `reduck/crunchbase.com/get_current_user`
- Updated: 2026-09-28 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/crunchbase.com/get_current_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/get_current_user
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `email` (string | null, optional)
- `lastName` (string | null, optional)
- `firstName` (string | null, optional)

## FAQ

### What does "Get Current User" do?

Report which Crunchbase account this browser is signed in as: email, first name and last name from Account Settings > Your Info. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Crunchbase scripts.

### How do I automatically get Current User on crunchbase.com?

Ask an AI agent connected to Reduck to run reduck/crunchbase.com/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/get_current_user

### Is there a crunchbase.com API to get Current User?

You do not need one. "Get Current User" drives the real crunchbase.com pages in a browser, so it works whether or not crunchbase.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns email, lastName, loggedIn, firstName.

### Do I need to be logged in to crunchbase.com?

Yes. It acts as you on crunchbase.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the crunchbase.com cookies saved by the Reduck extension.

### Does it change anything on crunchbase.com, or only read data?

It only reads. It looks things up on crunchbase.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/crunchbase.com/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/get_current_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/crunchbase.com/get_current_user
