# Export an X (Twitter) account's followers or following

Automatically export an X (Twitter) account's followers or following on x.com. List a user's followers or the accounts they follow, by handle — selected by the direction arg ('followers', the default, or 'following'). Returns per account: user_id, handle, name, followers, following, tweets, verified, location, website, bio. Scrolls until count is met or the list dries up.

- Site: x.com
- Address: `reduck/x.com/get_follows`
- Updated: 2026-10-22 (v12)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/get_follows`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/get_follows
```

## Input

- `count` (integer, optional): Max accounts to return. Scrolls until count is met or the list dries up. Default 100.
- `handle` (string, optional): Target user's handle (with or without @).
- `handles` (array, optional): Not supported since 19 Oct 2026: the run fails with a message saying so. Send one handle per call and fan out with run_script's scripts.
- `direction` (any, optional): Which list to read: the user's 'followers', or the accounts they follow ('following').

## Output

- `count` (integer, optional): Number of accounts returned. 0 is a first-class outcome (none, or protected/hidden).
- `handle` (string, optional)
- `accounts` (any, optional)
- `complete` (boolean, optional): True when X showed the end of the list and every account it sent is returned. False when more may exist: count was reached or X stopped loading.
- `direction` (string, optional)

## FAQ

### What does "Export an X (Twitter) account's followers or following" do?

List a user's followers or the accounts they follow, by handle — selected by the direction arg ('followers', the default, or 'following'). Returns per account: user_id, handle, name, followers, following, tweets, verified, location, website, bio. Scrolls until count is met or the list dries up.

### How do I automatically export an X (Twitter) account's followers or following on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/get_follows, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_follows

### Is there a x.com API to export an X (Twitter) account's followers or following?

You do not need one. "Export an X (Twitter) account's followers or following" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Optional: count, handle, handles, direction.

### What does it return?

It returns count, handle, accounts, complete, direction.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It only reads. It looks things up on x.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/get_follows, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_follows

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/get_follows
