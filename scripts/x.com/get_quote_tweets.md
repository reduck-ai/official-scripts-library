# Get the quote tweets of a post on X (Twitter)

Automatically get the quote tweets of a post on X (Twitter) on x.com. Each quoter's own comment, with handle, likes and views, up to 100 quotes per run.

- Site: x.com
- Address: `reduck/x.com/get_quote_tweets`
- Updated: 2026-10-05 (v1)
- Author: Reduck AI (reduck)

## About

Paste a post URL and you get back the quotes X lists under it, each with the quoter's own comment, handle, timestamp and engagement counts. The original post is not repeated, so pair this with get_tweet if you need its text and numbers. Say a SaaS founder tweets that the $12 plan is moving to $19 and has 70 quotes by lunch. With count raised to 100, they sort by views, leaving the few with null views at the bottom, and read the top five to see whether the angry takes are the ones getting seen. That decides who gets a reply first. The catch is that you only get what X's quotes list loads for your account, which leaves out quotes from protected accounts you don't follow. Scrolling also gives up after two scrolls in a row bring nothing new, so treat the count as what X served, not a census.

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

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "url": "https://example.com/item/123",
  "count": 3,
  "tweets": [
    {
      "id": "abc123",
      "url": "https://example.com/item/123",
      "lang": "…",
      "text": "…",
      "likes": 1200,
      "views": 1200,
      "author": {
        "id": "abc123",
        "name": "Example",
        "handle": "…"
      },
      "quotes": 3,
      "replies": 3,
      "is_quote": true,
      "retweets": 3,
      "bookmarks": 3,
      "created_at": "2026-01-15T09:30:00Z",
      "is_retweet": true
    }
  ]
}
```

## FAQ

### What does "Get the quote tweets of a post on X (Twitter)" do?

List the tweets that quote-tweeted a given X post, by post URL, including each quoter's own commentary. Returns per tweet a canonical record: id, url, author {id, handle, name}, text, created_at, lang, likes, retweets, replies, quotes, bookmarks, views, is_retweet, is_quote.

### How do I automatically get the quote tweets of a post on X (Twitter) on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/get_quote_tweets, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_quote_tweets

### Is there a x.com API to get the quote tweets of a post on X (Twitter)?

You do not need one. "Get the quote tweets of a post on X (Twitter)" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

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

### How many quote tweets can I get from one post?

One run returns up to 100 quote tweets, or 20 if you leave count unset. The script scrolls the post's quotes list until it reaches count or two scrolls in a row add nothing new. There is no cursor, so on a viral post with thousands of quotes you get the first 100 that X loads, and running it again starts from the top rather than picking up where it stopped.

### Where do I see the quote tweets of a post on X itself?

On X, click the repost icon under the post and choose View Quotes, which opens the post's own URL with /quotes added at the end. The script reads that same list in your signed-in browser, so you get what you would see by scrolling it yourself. Plain reposts are not in that list; get_reposters returns a sample of those accounts, with follower counts.

### How much would the same data cost through the official X API?

As of October 2026, X's pay-per-use pricing lists a post read at $0.005, so 100 quotes from GET /2/tweets/:id/quote_tweets (10 to 100 results per page) come to about $0.50. Looking up each quoter's profile on top of that is listed separately at $0.010 per user read.

### How do I find which quoters have the biggest audience?

This output has no follower counts for the quoters, so sort by views first and keep the ten or so quotes that travelled furthest. Then run get_user_info on those author.handle values for an exact followers_count; it takes one handle per run, so looking up all 100 quoters is rarely worth it.

Source: https://reduck.ai/explore/scripts/reduck/x.com/get_quote_tweets
