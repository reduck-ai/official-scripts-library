# Get Reddit user profile

Automatically get Reddit user profile on reddit.com. Fetch a Reddit user's profile by their username (with or without the u/ prefix). Returns username, display_name, description, karma, contributions, reddit_age, and one page of recent posts and comments (type, title, text, subreddit, score, created, url). Recent activity is empty when the account hides it or has none. Pass the returned nextCursor as cursor to read the next page of recent activity; it is null on the last page.

- Site: reddit.com
- Address: `reduck/reddit.com/get_user`
- Updated: 2026-10-22 (v13)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/reddit.com/get_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_user
```

## Input

- `username` (string, required): Reddit username, with or without the u/ prefix
- `cursor` (string, optional): The nextCursor of the previous answer, to read the next page of recent posts and comments. Omit for the first page.

## Output

- `karma` (integer | null, required): Total karma, post plus comment karma, exact.
- `recent` (array, required): Recent posts and comments from the profile's overview feed. Empty when the account hides its posts, which is a real outcome rather than a session effect.
- `username` (string, required)
- `nextCursor` (string | null, required): Pass as cursor to read the next page of recent activity; null on the last page.
- `cake_day` (string | null, optional): Date the account was created (ISO 8601).
- `post_karma` (integer | null, optional)
- `description` (string | null, optional)
- `display_name` (string | null, optional)
- `comment_karma` (integer | null, optional)
- `contributions` (integer | null, optional): Contribution count; null when Reddit shows it abbreviated.

## FAQ

### What does "Get Reddit user profile" do?

Fetch a Reddit user's profile by their username (with or without the u/ prefix). Returns username, display_name, description, karma, contributions, reddit_age, and one page of recent posts and comments (type, title, text, subreddit, score, created, url). Recent activity is empty when the account hides it or has none. Pass the returned nextCursor as cursor to read the next page of recent activity; it is null on the last page.

### How do I automatically get Reddit user profile on reddit.com?

Ask an AI agent connected to Reduck to run reduck/reddit.com/get_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_user

### Is there a reddit.com API to get Reddit user profile?

You do not need one. "Get Reddit user profile" drives the real reddit.com pages in a browser, so it works whether or not reddit.com offers an API for this.

### What information do I need to provide?

Required: username. Optional: cursor.

### What does it return?

It returns karma, recent, cake_day, username, nextCursor, post_karma, description, display_name, comment_karma, contributions.

### Do I need to be logged in to reddit.com?

No. It only uses pages of reddit.com that are reachable without signing in.

### Does it change anything on reddit.com, or only read data?

It only reads. It looks things up on reddit.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/reddit.com/get_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/reddit.com/get_user
