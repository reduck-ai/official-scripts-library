# Get LinkedIn feed posts

Automatically get LinkedIn feed posts on linkedin.com. Get posts from the logged-in user's LinkedIn home feed (linkedin.com/feed/), scrolling to load up to count posts. Returns each post's author (name, headline, connection degree, profile URL, profile picture), text, age, engagement counts, sponsored flag, permalink, any quoted post, and the feed's reason line verbatim - why the post is there ("X reposted this", "X commented", "Suggested") - with a profile URL for each actor it names. The reason line is never classified into a flag: its wording is localized and open-ended, so read reason.text to tell a repost from a like. authorPictureUrl is a signed media.licdn.com CDN link, not a stable reference: it carries an expiry a few weeks out and 403s if the query string is altered, so pass it through whole and download the bytes if you need the image to outlive the link - never store the URL. Join on authorProfileUrl instead.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_feed_posts`
- Updated: 2026-09-03 (v12)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_feed_posts`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_feed_posts
```

## Input

- `count` (integer, optional): Max posts to collect by scrolling the home feed. Default 10; the feed is effectively infinite (algorithmic recommendations), so this is the only bound.

## Output

- `posts` (array, required)

## FAQ

### What does "Get LinkedIn feed posts" do?

Get posts from the logged-in user's LinkedIn home feed (linkedin.com/feed/), scrolling to load up to count posts. Returns each post's author (name, headline, connection degree, profile URL, profile picture), text, age, engagement counts, sponsored flag, permalink, any quoted post, and the feed's reason line verbatim - why the post is there ("X reposted this", "X commented", "Suggested") - with a profile URL for each actor it names. The reason line is never classified into a flag: its wording is localized and open-ended, so read reason.text to tell a repost from a like. authorPictureUrl is a signed media.licdn.com CDN link, not a stable reference: it carries an expiry a few weeks out and 403s if the query string is altered, so pass it through whole and download the bytes if you need the image to outlive the link - never store the URL. Join on authorProfileUrl instead.

### How do I automatically get LinkedIn feed posts on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_feed_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_feed_posts

### Is there a linkedin.com API to get LinkedIn feed posts?

You do not need one. "Get LinkedIn feed posts" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Optional: count.

### What does it return?

It returns posts.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_feed_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_feed_posts

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_feed_posts
