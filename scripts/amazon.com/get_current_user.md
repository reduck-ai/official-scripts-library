# Get current Amazon user

Automatically get current Amazon user on amazon.com. Report whether this browser is signed in to Amazon.com and, if so, the account's first name from the header greeting (Amazon hides the full name and email behind a password re-check). Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Amazon scripts.

- Site: amazon.com
- Address: `reduck/amazon.com/get_current_user`
- Updated: 2026-09-28 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.com/get_current_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.com/get_current_user
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `firstName` (string | null, optional)

## FAQ

### What does "Get current Amazon user" do?

Report whether this browser is signed in to Amazon.com and, if so, the account's first name from the header greeting (Amazon hides the full name and email behind a password re-check). Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Amazon scripts.

### How do I automatically get current Amazon user on amazon.com?

Ask an AI agent connected to Reduck to run reduck/amazon.com/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com/get_current_user

### Is there a amazon.com API to get current Amazon user?

You do not need one. "Get current Amazon user" drives the real amazon.com pages in a browser, so it works whether or not amazon.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns loggedIn, firstName.

### Do I need to be logged in to amazon.com?

Yes. It acts as you on amazon.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the amazon.com cookies saved by the Reduck extension.

### Does it change anything on amazon.com, or only read data?

It only reads. It looks things up on amazon.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.com/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com/get_current_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/amazon.com/get_current_user
