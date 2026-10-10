# Get subreddit info

Automatically get subreddit info on reddit.com. Fetch a subreddit's metadata: title, description, created date, weekly visitors and contributions, its type (public, restricted…), every rule (title and body), and its full moderator list with each moderator's permissions and join date. A banned or private subreddit returns its status and nothing else; an unknown name throws. The moderator list is null when Reddit does not show it to the browser's session.

- Site: reddit.com
- Address: `reduck/reddit.com/get_subreddit_info`
- Updated: 2026-10-09 (v12)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/reddit.com/get_subreddit_info`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_subreddit_info
```

## Input

- `subreddit` (string, required): Subreddit name, with or without the r/ prefix

## Output

- `status` (string, required): How Reddit classifies the subreddit: for a live one its subreddit_type ("public", "restricted", "user", ...); for one that cannot be read, the gate ("banned", "private", "gold_only").
- `subreddit` (string, required)
- `id` (string | null, optional)
- `rules` (array | null, optional)
- `title` (string | null, optional)
- `detail` (string | null, optional): For a gated or banned subreddit, Reddit's own reason code ("banned", "private", "gold_only"); null when the subreddit is live.
- `created` (string | null, optional)
- `moderators` (array | null, optional): Every moderator, in Reddit's order. null when Reddit does not show the list to this browser's session.
- `description` (string | null, optional)
- `weekly_active_users` (number | null, optional)
- `weekly_contributions` (number | null, optional)

## FAQ

### What does "Get subreddit info" do?

Fetch a subreddit's metadata: title, description, created date, weekly visitors and contributions, its type (public, restricted…), every rule (title and body), and its full moderator list with each moderator's permissions and join date. A banned or private subreddit returns its status and nothing else; an unknown name throws. The moderator list is null when Reddit does not show it to the browser's session.

### How do I automatically get subreddit info on reddit.com?

Ask an AI agent connected to Reduck to run reduck/reddit.com/get_subreddit_info, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_subreddit_info

### Is there a reddit.com API to get subreddit info?

You do not need one. "Get subreddit info" drives the real reddit.com pages in a browser, so it works whether or not reddit.com offers an API for this.

### What information do I need to provide?

Required: subreddit.

### What does it return?

It returns id, rules, title, detail, status, created, subreddit, moderators, description, weekly_active_users, weekly_contributions.

### Do I need to be logged in to reddit.com?

No. It only uses pages of reddit.com that are reachable without signing in.

### Does it change anything on reddit.com, or only read data?

It only reads. It looks things up on reddit.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/reddit.com/get_subreddit_info, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_subreddit_info

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/reddit.com/get_subreddit_info
