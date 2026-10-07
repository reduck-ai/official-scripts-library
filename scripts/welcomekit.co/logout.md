# Welcome to the Jungle logout

Sign out of the Welcome to the Jungle recruiting dashboard (welcomekit.co) in this browser. If no session is open it returns straight away and says so. Returns whether a session was open and whether the browser is now signed out. It only ends the Welcome to the Jungle session, not the browser's Google session.

- Site: welcomekit.co
- Address: `reduck/welcomekit.co/logout`
- Updated: 2026-10-06 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/welcomekit.co/logout`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/logout
```

## Input

It takes no input.

## Output

- `url` (string, required)
- `loggedOut` (boolean, required)
- `wasLoggedIn` (boolean, required)

## FAQ

### What does "Welcome to the Jungle logout" do?

Sign out of the Welcome to the Jungle recruiting dashboard (welcomekit.co) in this browser. If no session is open it returns straight away and says so. Returns whether a session was open and whether the browser is now signed out. It only ends the Welcome to the Jungle session, not the browser's Google session.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns url, loggedOut, wasLoggedIn.

### Do I need to be logged in to welcomekit.co?

No. It only uses pages of welcomekit.co that are reachable without signing in.

### Does it change anything on welcomekit.co, or only read data?

It makes changes on welcomekit.co, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/welcomekit.co/logout, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/logout

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/welcomekit.co/logout
