# Get Reddit user profile

Automatically get Reddit user profile on reddit.com. Fetch a Reddit user's profile by their username (with or without the u/ prefix). Returns username, display_name, description, karma, contributions, reddit_age, and recent posts and comments (type, title, text, subreddit, score, created, url).

- Site: reddit.com
- Address: `reduck/reddit.com/get_user`
- Updated: 2026-09-08 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/reddit.com/get_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_user
```

## Input

- `username` (string, required): Reddit username, with or without the u/ prefix
- `limit` (integer, optional): Max number of recent posts/comments to return (slices the SSR'd overview feed). Default 25.

## Output

- `karma` (string | null, required): As displayed (may be abbreviated, e.g. "16.7k")
- `recent` (array, required): Recent posts and comments from the SSR'd overview feed. Empty when the account hides its posts, which is a real outcome rather than a session effect.
- `username` (string, required)
- `reddit_age` (string | null, optional): As displayed, e.g. "10 y"
- `description` (string | null, optional)
- `display_name` (string | null, optional)
- `contributions` (string | null, optional)

## FAQ

### What does "Get Reddit user profile" do?

Fetch a Reddit user's profile by their username (with or without the u/ prefix). Returns username, display_name, description, karma, contributions, reddit_age, and recent posts and comments (type, title, text, subreddit, score, created, url).

### How do I automatically get Reddit user profile on reddit.com?

Ask an AI agent connected to Reduck to run reduck/reddit.com/get_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_user

### Is there a reddit.com API to get Reddit user profile?

You do not need one. "Get Reddit user profile" drives the real reddit.com pages in a browser, so it works whether or not reddit.com offers an API for this.

### What information do I need to provide?

Required: username. Optional: limit.

### What does it return?

It returns karma, recent, username, reddit_age, description, display_name, contributions.

### Do I need to be logged in to reddit.com?

No. It only uses pages of reddit.com that are reachable without signing in.

### Does it change anything on reddit.com, or only read data?

It only reads. It looks things up on reddit.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/reddit.com/get_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/reddit.com/get_user
