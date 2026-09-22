# Get own Instagram profile

Automatically get own Instagram profile on instagram.com. Read the logged-in Instagram account's own profile: handle, display name, bio, follower / following / post counts, profile picture and whether the account is private, verified or a business account.

- Site: instagram.com
- Address: `reduck/instagram.com/get_own_profile`
- Updated: 2026-09-17 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/get_own_profile`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_own_profile
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required): Whether this browser has a usable Instagram session. False is a normal result, not a failure, so this can be polled on a schedule without the check counting against its own health.
- `bio` (string | null, optional)
- `name` (string | null, optional): Display / full name.
- `handle` (string | null, optional): The logged-in account's username, without @. Null when there is no session.
- `userId` (string | null, optional)
- `evidence` (string | null, optional): Only set when loggedIn is false: what proved the session absent, so a genuine signed-out reading can be told from a broken run.
- `isPrivate` (boolean | null, optional)
- `isBusiness` (boolean | null, optional)
- `isVerified` (boolean | null, optional)
- `postsCount` (integer | null, optional)
- `externalUrl` (string | null, optional)
- `profilePicUrl` (string | null, optional)
- `followersCount` (integer | null, optional)
- `followingCount` (integer | null, optional)

## FAQ

### What does "Get own Instagram profile" do?

Read the logged-in Instagram account's own profile: handle, display name, bio, follower / following / post counts, profile picture and whether the account is private, verified or a business account.

### How do I automatically get own Instagram profile on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_own_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_own_profile

### Is there a instagram.com API to get own Instagram profile?

You do not need one. "Get own Instagram profile" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns bio, name, handle, userId, evidence, loggedIn, isPrivate, isBusiness, isVerified, postsCount, externalUrl, profilePicUrl, followersCount, followingCount.

### Do I need to be logged in to instagram.com?

No. It only uses pages of instagram.com that are reachable without signing in.

### Does it change anything on instagram.com, or only read data?

It only reads. It looks things up on instagram.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_own_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_own_profile

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/get_own_profile
