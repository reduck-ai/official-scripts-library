# Get Reddit user comments

Automatically get Reddit user comments on reddit.com. Fetch a Reddit user's recent comments from their profile Comments tab (with or without u/ prefix). Returns subreddit, post title/url, comment body/permalink, score, timestamp, and stickied flag. Scrolls to load more when limit exceeds one page.

- Site: reddit.com
- Address: `reduck/reddit.com/get_user_comments`
- Updated: 2026-09-03 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/reddit.com/get_user_comments`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_user_comments
```

## Input

- `username` (string, required): Reddit username, with or without the u/ prefix
- `limit` (integer, optional): Max number of comments to return. Scrolls to load more pages as needed.

## Output

- `comments` (array, required)
- `username` (string, required)

## FAQ

### What does "Get Reddit user comments" do?

Fetch a Reddit user's recent comments from their profile Comments tab (with or without u/ prefix). Returns subreddit, post title/url, comment body/permalink, score, timestamp, and stickied flag. Scrolls to load more when limit exceeds one page.

### How do I automatically get Reddit user comments on reddit.com?

Ask an AI agent connected to Reduck to run reduck/reddit.com/get_user_comments, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_user_comments

### Is there a reddit.com API to get Reddit user comments?

You do not need one. "Get Reddit user comments" drives the real reddit.com pages in a browser, so it works whether or not reddit.com offers an API for this.

### What information do I need to provide?

Required: username. Optional: limit.

### What does it return?

It returns comments, username.

### Do I need to be logged in to reddit.com?

No. It only uses pages of reddit.com that are reachable without signing in.

### Does it change anything on reddit.com, or only read data?

It only reads. It looks things up on reddit.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/reddit.com/get_user_comments, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_user_comments

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/reddit.com/get_user_comments
