# Discord login

Opens the Discord web app in the browser and reports whether the account is signed in, together with the username and display name it is signed in as. Run this first: the other Discord scripts need the web app open on a signed-in session.

- Site: discord.com
- Address: `reduck/discord.com/login`
- Updated: 2026-09-18 (v14)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/discord.com/login`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/discord.com/login
```

## Input

It takes no input.

## Output

- `url` (string, required)
- `state` (string, required): Which surface the browser landed on. "app" is the signed-in web app. "login" is Discord's login page. "anonymous" is the marketing homepage still offering guest onboarding, which a signed-out browser reaches without ever being redirected to /login. Both of the latter two mean loggedIn is false.
- `loggedIn` (boolean, required): True only when the browser landed on the signed-in web app. A signed-out browser is a normal result reported as false, not an error.
- `username` (string | null, optional): Null unless loggedIn is true.
- `displayName` (string | null, optional): Null unless loggedIn is true.

## FAQ

### What does "Discord login" do?

Opens the Discord web app in the browser and reports whether the account is signed in, together with the username and display name it is signed in as. Run this first: the other Discord scripts need the web app open on a signed-in session.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns url, state, loggedIn, username, displayName.

### Do I need to be logged in to discord.com?

Yes. It acts as you on discord.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the discord.com cookies saved by the Reduck extension.

### Does it change anything on discord.com, or only read data?

It only reads. It looks things up on discord.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/discord.com/login, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/login

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/discord.com/login
