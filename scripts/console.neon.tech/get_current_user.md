# Get current Neon console user

Automatically get current Neon console user on console.neon.tech. Report which Neon console account this browser is signed in as: email, first name and last name. When the browser is signed out of the Neon console, the run fails with a signed-out error asking you to sign in to console.neon.tech.

- Site: console.neon.tech
- Address: `reduck/console.neon.tech/get_current_user`
- Updated: 2026-10-27 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/console.neon.tech/get_current_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/console.neon.tech/get_current_user
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `email` (string | null, optional)
- `lastName` (string | null, optional)
- `firstName` (string | null, optional)

## FAQ

### What does "Get current Neon console user" do?

Report which Neon console account this browser is signed in as: email, first name and last name. When the browser is signed out of the Neon console, the run fails with a signed-out error asking you to sign in to console.neon.tech.

### How do I automatically get current Neon console user on console.neon.tech?

Ask an AI agent connected to Reduck to run reduck/console.neon.tech/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/console.neon.tech/get_current_user

### Is there a console.neon.tech API to get current Neon console user?

You do not need one. "Get current Neon console user" drives the real console.neon.tech pages in a browser, so it works whether or not console.neon.tech offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns email, lastName, loggedIn, firstName.

### Do I need to be logged in to console.neon.tech?

Yes. It acts as you on console.neon.tech: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the console.neon.tech cookies saved by the Reduck extension.

### Does it change anything on console.neon.tech, or only read data?

It only reads. It looks things up on console.neon.tech and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/console.neon.tech/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/console.neon.tech/get_current_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/console.neon.tech/get_current_user
