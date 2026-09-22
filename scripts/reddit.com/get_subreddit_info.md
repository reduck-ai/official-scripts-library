# Get subreddit info

Automatically get subreddit info on reddit.com. Fetch a subreddit's metadata from its page: title, description, weekly active users / contributions, created date, visibility, rules (title + body), and the full moderator list (username, permissions, joined). Banned/private subs return status with detail; unknown subs throw.

- Site: reddit.com
- Address: `reduck/reddit.com/get_subreddit_info`
- Updated: 2026-09-15 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/reddit.com/get_subreddit_info`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_subreddit_info
```

## Input

- `subreddit` (string, required): Subreddit name, with or without the r/ prefix

## Output

- `status` (string, required): How reddit itself classifies the subreddit. For a live one this is about.json's subreddit_type ("public", "restricted", "user", ...). For one that cannot be read it is the gate: "banned", "missing" (never existed), "private", or "gold_only". Sourced entirely from about.json rather than from rendered page copy, so it does not change with the interface language.
- `subreddit` (string, required)
- `id` (string | null, optional)
- `rules` (array | null, optional)
- `title` (string | null, optional)
- `detail` (string | null, optional): For a gated or banned subreddit, reddit's own machine reason code from about.json - "banned", "private", "gold_only" - or null when the subreddit is live or simply never existed. Before v5 this was an English sentence scraped off the page; it is now a code, so it is stable across languages and comparable.
- `created` (string | null, optional)
- `moderators` (array | null, optional)
- `description` (string | null, optional)
- `weekly_active_users` (number | null, optional)
- `weekly_contributions` (number | null, optional)

## FAQ

### What does "Get subreddit info" do?

Fetch a subreddit's metadata from its page: title, description, weekly active users / contributions, created date, visibility, rules (title + body), and the full moderator list (username, permissions, joined). Banned/private subs return status with detail; unknown subs throw.

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
