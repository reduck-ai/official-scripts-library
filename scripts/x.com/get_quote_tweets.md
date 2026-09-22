# Get X quote tweets

Automatically get X quote tweets on x.com. List the tweets that quote-tweeted a given X post, by post URL, including each quoter's own commentary. Returns per tweet a canonical record: id, url, author {id, handle, name}, text, created_at, lang, likes, retweets, replies, quotes, bookmarks, views, is_retweet, is_quote.

- Site: x.com
- Address: `reduck/x.com/get_quote_tweets`
- Updated: 2026-09-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/get_quote_tweets`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/get_quote_tweets
```

## Input

- `url` (string, required): Full URL of the X post whose quote-tweets you want, e.g. 'https://x.com/<handle>/status/<id>'. Query/hash are stripped.
- `count` (integer, optional): Max quote-tweets to return. Scrolls until count is met or results dry up. Default 20, max 100.

## Output

- `url` (string, required)
- `count` (integer, required): Number of quote-tweets returned. 0 is a first-class outcome (no quotes).
- `tweets` (array, required)

## FAQ

### What does "Get X quote tweets" do?

List the tweets that quote-tweeted a given X post, by post URL, including each quoter's own commentary. Returns per tweet a canonical record: id, url, author {id, handle, name}, text, created_at, lang, likes, retweets, replies, quotes, bookmarks, views, is_retweet, is_quote.

### How do I automatically get X quote tweets on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/get_quote_tweets, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_quote_tweets

### Is there a x.com API to get X quote tweets?

You do not need one. "Get X quote tweets" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Required: url. Optional: count.

### What does it return?

It returns url, count, tweets.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It only reads. It looks things up on x.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/get_quote_tweets, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_quote_tweets

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/get_quote_tweets
