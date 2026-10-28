# Get current YouTube user

Automatically get current YouTube user on youtube.com. Report which Google/YouTube account this browser is signed in as: the account email. When the browser is signed out of YouTube, including when YouTube shows its cookie-consent page to a visitor with no signed-in account, the run fails with a signed-out error asking you to sign in to youtube.com.

- Site: youtube.com
- Address: `reduck/youtube.com/get_current_user`
- Updated: 2026-10-22 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/youtube.com/get_current_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/youtube.com/get_current_user
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `note` (string | null, optional): Always null: a signed-out browser, including one YouTube sends to its cookie-consent page, fails with a signed-out error.
- `email` (string | null, optional)

## FAQ

### What does "Get current YouTube user" do?

Report which Google/YouTube account this browser is signed in as: the account email. When the browser is signed out of YouTube, including when YouTube shows its cookie-consent page to a visitor with no signed-in account, the run fails with a signed-out error asking you to sign in to youtube.com.

### How do I automatically get current YouTube user on youtube.com?

Ask an AI agent connected to Reduck to run reduck/youtube.com/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/youtube.com/get_current_user

### Is there a youtube.com API to get current YouTube user?

You do not need one. "Get current YouTube user" drives the real youtube.com pages in a browser, so it works whether or not youtube.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns note, email, loggedIn.

### Do I need to be logged in to youtube.com?

Yes. It acts as you on youtube.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the youtube.com cookies saved by the Reduck extension.

### Does it change anything on youtube.com, or only read data?

It only reads. It looks things up on youtube.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/youtube.com/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/youtube.com/get_current_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/youtube.com/get_current_user
