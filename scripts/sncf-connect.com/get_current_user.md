# Get the signed-in SNCF Connect user

Automatically get the signed-in SNCF Connect user on sncf-connect.com. Report which SNCF Connect account this browser is signed in as: name and email from the account's personal space. When the browser is not signed in to SNCF Connect, the run fails with a signed-out error asking you to sign in, then retry.

- Site: sncf-connect.com
- Address: `reduck/sncf-connect.com/get_current_user`
- Updated: 2026-10-20 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/sncf-connect.com/get_current_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/sncf-connect.com/get_current_user
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional)

## FAQ

### What does "Get the signed-in SNCF Connect user" do?

Report which SNCF Connect account this browser is signed in as: name and email from the account's personal space. When the browser is not signed in to SNCF Connect, the run fails with a signed-out error asking you to sign in, then retry.

### How do I automatically get the signed-in SNCF Connect user on sncf-connect.com?

Ask an AI agent connected to Reduck to run reduck/sncf-connect.com/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/sncf-connect.com/get_current_user

### Is there a sncf-connect.com API to get the signed-in SNCF Connect user?

You do not need one. "Get the signed-in SNCF Connect user" drives the real sncf-connect.com pages in a browser, so it works whether or not sncf-connect.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email, loggedIn.

### Do I need to be logged in to sncf-connect.com?

Yes. It acts as you on sncf-connect.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the sncf-connect.com cookies saved by the Reduck extension.

### Does it change anything on sncf-connect.com, or only read data?

It only reads. It looks things up on sncf-connect.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/sncf-connect.com/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/sncf-connect.com/get_current_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/sncf-connect.com/get_current_user
