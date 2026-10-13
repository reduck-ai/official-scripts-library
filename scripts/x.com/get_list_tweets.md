# Read an X (Twitter) List's timeline

Automatically read an X (Twitter) List's timeline on x.com. Read the timeline of an X list — the tweets from its member accounts, newest first, given the list's URL or id. Returns per tweet a canonical record: id, url, author {id, handle, name}, text, created_at, lang, likes, retweets, replies, quotes, bookmarks, views, is_retweet, is_quote.

- Site: x.com
- Address: `reduck/x.com/get_list_tweets`
- Updated: 2026-10-12 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/get_list_tweets`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/get_list_tweets
```

## Input

- `list` (string, required): The list's numeric id (e.g. '1272593321181851648'), or any X URL containing it (e.g. 'https://x.com/i/lists/1272593321181851648').
- `count` (integer, optional): How many to return. Without it, the script returns the first page X shows (often 20 to 40). With it, the script loads more until it has count, reaches the end, or X stops loading; complete says whether it reached the end.

## Output

- `count` (integer, required): Number of tweets returned. 0 is a valid answer.
- `tweets` (array, required)
- `list_id` (string, required)
- `complete` (boolean, required): True when X showed the end of the list's timeline and every one it sent is returned. False when there may be more: count was reached, X stopped loading, or no count was given and the first page is not the end.

## FAQ

### What does "Read an X (Twitter) List's timeline" do?

Read the timeline of an X list — the tweets from its member accounts, newest first, given the list's URL or id. Returns per tweet a canonical record: id, url, author {id, handle, name}, text, created_at, lang, likes, retweets, replies, quotes, bookmarks, views, is_retweet, is_quote.

### How do I automatically read an X (Twitter) List's timeline on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/get_list_tweets, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_list_tweets

### Is there a x.com API to read an X (Twitter) List's timeline?

You do not need one. "Read an X (Twitter) List's timeline" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Required: list. Optional: count.

### What does it return?

It returns count, tweets, list_id, complete.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It only reads. It looks things up on x.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/get_list_tweets, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_list_tweets

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/get_list_tweets
