# Get Reddit user comments

Automatically get Reddit user comments on reddit.com. Fetch a Reddit user's recent comments from their profile Comments tab (with or without u/ prefix), one page at a time, newest first. Returns subreddit, post title/url, comment body/permalink, score, timestamp, and stickied flag. A profile with no comments returns an empty list; an unknown user fails. Pass the returned nextCursor as cursor to read the next page; it is null on the last page.

- Site: reddit.com
- Address: `reduck/reddit.com/get_user_comments`
- Updated: 2026-10-22 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/reddit.com/get_user_comments`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_user_comments
```

## Input

- `username` (string, required): Reddit username, with or without the u/ prefix
- `cursor` (string, optional): The nextCursor of the previous answer, to read the next page. Omit for the first page.

## Output

- `comments` (array, required)
- `username` (string, required)
- `nextCursor` (string | null, required): Pass as cursor to read the next page; null on the last page.

## FAQ

### What does "Get Reddit user comments" do?

Fetch a Reddit user's recent comments from their profile Comments tab (with or without u/ prefix), one page at a time, newest first. Returns subreddit, post title/url, comment body/permalink, score, timestamp, and stickied flag. A profile with no comments returns an empty list; an unknown user fails. Pass the returned nextCursor as cursor to read the next page; it is null on the last page.

### How do I automatically get Reddit user comments on reddit.com?

Ask an AI agent connected to Reduck to run reduck/reddit.com/get_user_comments, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_user_comments

### Is there a reddit.com API to get Reddit user comments?

You do not need one. "Get Reddit user comments" drives the real reddit.com pages in a browser, so it works whether or not reddit.com offers an API for this.

### What information do I need to provide?

Required: username. Optional: cursor.

### What does it return?

It returns comments, username, nextCursor.

### Do I need to be logged in to reddit.com?

No. It only uses pages of reddit.com that are reachable without signing in.

### Does it change anything on reddit.com, or only read data?

It only reads. It looks things up on reddit.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/reddit.com/get_user_comments, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_user_comments

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/reddit.com/get_user_comments
