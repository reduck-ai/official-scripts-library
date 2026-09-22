# Get X follows

Automatically get X follows on x.com. List a user's followers or the accounts they follow, by handle — selected by the direction arg ('followers', the default, or 'following'). Returns per account: user_id, handle, name, followers, following, tweets, verified, location, website, bio. Scrolls until count is met or the list dries up.

- Site: x.com
- Address: `reduck/x.com/get_follows`
- Updated: 2026-09-03 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/get_follows`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/get_follows
```

## Input

- `handle` (string, required): Target user's handle (with or without @).
- `count` (integer, optional): Max accounts to return. Scrolls until count is met or the list dries up. Default 100.
- `direction` (any, optional): Which list to read: the user's 'followers', or the accounts they follow ('following').

## Output

- `count` (integer, required): Number of accounts returned. 0 is a first-class outcome (none, or protected/hidden).
- `handle` (string, required)
- `accounts` (array, required)
- `direction` (string, required)

## FAQ

### What does "Get X follows" do?

List a user's followers or the accounts they follow, by handle — selected by the direction arg ('followers', the default, or 'following'). Returns per account: user_id, handle, name, followers, following, tweets, verified, location, website, bio. Scrolls until count is met or the list dries up.

### How do I automatically get X follows on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/get_follows, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_follows

### Is there a x.com API to get X follows?

You do not need one. "Get X follows" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Required: handle. Optional: count, direction.

### What does it return?

It returns count, handle, accounts, direction.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It only reads. It looks things up on x.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/get_follows, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_follows

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/get_follows
