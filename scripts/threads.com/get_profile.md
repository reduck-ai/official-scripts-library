# Get Threads profile

Automatically get Threads profile on threads.com. Fetch a Threads user's profile: display name, bio, avatar, website, topic tags, and follower count.

- Site: threads.com
- Address: `reduck/threads.com/get_profile`
- Updated: 2026-09-03 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/threads.com/get_profile`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/threads.com/get_profile
```

## Input

- `username` (string, required): Threads username, with or without the leading @

## Output

- `found` (boolean, required): false if the username doesn't resolve to a viewable profile
- `username` (string, required)
- `bio` (string | null, optional)
- `tags` (array, optional)
- `website` (string | null, optional)
- `avatarUrl` (string | null, optional)
- `displayName` (string | null, optional)
- `followersText` (string | null, optional): Raw follower count as displayed (locale-formatted, e.g. '12,6 M followers')

## FAQ

### What does "Get Threads profile" do?

Fetch a Threads user's profile: display name, bio, avatar, website, topic tags, and follower count.

### How do I automatically get Threads profile on threads.com?

Ask an AI agent connected to Reduck to run reduck/threads.com/get_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/threads.com/get_profile

### Is there a threads.com API to get Threads profile?

You do not need one. "Get Threads profile" drives the real threads.com pages in a browser, so it works whether or not threads.com offers an API for this.

### What information do I need to provide?

Required: username.

### What does it return?

It returns bio, tags, found, website, username, avatarUrl, displayName, followersText.

### Do I need to be logged in to threads.com?

No. It only uses pages of threads.com that are reachable without signing in.

### Does it change anything on threads.com, or only read data?

It only reads. It looks things up on threads.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/threads.com/get_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/threads.com/get_profile

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/threads.com/get_profile
