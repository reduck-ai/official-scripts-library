# Get current Semrush user

Automatically get current Semrush user on semrush.com. Returns the Semrush account currently signed in: user id, email, name and sign-up date.

- Site: semrush.com
- Address: `reduck/semrush.com/get_current_user`
- Updated: 2026-10-06 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/semrush.com/get_current_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/semrush.com/get_current_user
```

## Input

It takes no input.

## Output

- `id` (integer, required)
- `email` (string, required)
- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `registrationDate` (string | null, optional)

## FAQ

### What does "Get current Semrush user" do?

Returns the Semrush account currently signed in: user id, email, name and sign-up date.

### How do I automatically get current Semrush user on semrush.com?

Ask an AI agent connected to Reduck to run reduck/semrush.com/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/semrush.com/get_current_user

### Is there a semrush.com API to get current Semrush user?

You do not need one. "Get current Semrush user" drives the real semrush.com pages in a browser, so it works whether or not semrush.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns id, name, email, loggedIn, registrationDate.

### Do I need to be logged in to semrush.com?

Yes. It acts as you on semrush.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the semrush.com cookies saved by the Reduck extension.

### Does it change anything on semrush.com, or only read data?

It only reads. It looks things up on semrush.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/semrush.com/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/semrush.com/get_current_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/semrush.com/get_current_user
