# Get X list tweets

Automatically get X list tweets on x.com. Read the timeline of an X list — the tweets from its member accounts, newest first, given the list's URL or id. Returns per tweet a canonical record: id, url, author {id, handle, name}, text, created_at, lang, likes, retweets, replies, quotes, bookmarks, views, is_retweet, is_quote.

- Site: x.com
- Address: `reduck/x.com/get_list_tweets`
- Updated: 2026-09-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/get_list_tweets`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/get_list_tweets
```

## Input

- `list` (string, required): The list's numeric id (e.g. '1272593321181851648'), or any X URL containing it (e.g. 'https://x.com/i/lists/1272593321181851648' or a list's 'https://x.com/<handle>/lists/<slug>' page — the id is read from wherever it appears).
- `count` (integer, optional): Max tweets to return. Scrolls until count is met or the list dries up. Default 20, max 100.

## Output

- `count` (integer, required): Number of tweets returned. 0 is a first-class outcome (empty list).
- `tweets` (array, required)
- `list_id` (string, required)

## FAQ

### What does "Get X list tweets" do?

Read the timeline of an X list — the tweets from its member accounts, newest first, given the list's URL or id. Returns per tweet a canonical record: id, url, author {id, handle, name}, text, created_at, lang, likes, retweets, replies, quotes, bookmarks, views, is_retweet, is_quote.

### How do I automatically get X list tweets on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/get_list_tweets, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_list_tweets

### Is there a x.com API to get X list tweets?

You do not need one. "Get X list tweets" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Required: list. Optional: count.

### What does it return?

It returns count, tweets, list_id.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It only reads. It looks things up on x.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/get_list_tweets, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_list_tweets

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/get_list_tweets
