# Follow a Threads account

Automatically follow a Threads account on threads.com. Follow a Threads account by username, as the signed-in account. Reports whether the account was already followed so a repeat run does not toggle it off.

- Site: threads.com
- Address: `reduck/threads.com/follow_user`
- Updated: 2026-09-21 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/threads.com/follow_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/threads.com/follow_user
```

## Input

- `username` (string, required): Threads username to follow, with or without a leading @.

## Output

- `username` (string, required): The normalised username that was acted on (lower-cased, no leading @).
- `following` (boolean, required): True when the signed-in account follows this account after the run.
- `profileUrl` (string, required): The Threads profile URL.
- `alreadyFollowing` (boolean, required): True when the account was already followed before this run, in which case nothing was clicked.
- `followersText` (string | null, optional): The follower count as the profile displays it, verbatim (e.g. "5.5M followers"). A display string, not a number.

## FAQ

### What does "Follow a Threads account" do?

Follow a Threads account by username, as the signed-in account. Reports whether the account was already followed so a repeat run does not toggle it off.

### How do I automatically follow a Threads account on threads.com?

Ask an AI agent connected to Reduck to run reduck/threads.com/follow_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/threads.com/follow_user

### Is there a threads.com API to follow a Threads account?

You do not need one. "Follow a Threads account" drives the real threads.com pages in a browser, so it works whether or not threads.com offers an API for this.

### What information do I need to provide?

Required: username.

### What does it return?

It returns username, following, profileUrl, followersText, alreadyFollowing.

### Do I need to be logged in to threads.com?

Yes. It acts as you on threads.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the threads.com cookies saved by the Reduck extension.

### Does it change anything on threads.com, or only read data?

It makes changes on threads.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/threads.com/follow_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/threads.com/follow_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/threads.com/follow_user
