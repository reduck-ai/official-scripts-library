# Read an X (Twitter) Article

Automatically read an X (Twitter) Article on x.com. Read a long-form X (Twitter) Article from its link: title, author, publish date, cover image, engagement counts, and the full body in reading order, with its headings, lists, quotes, links, images, videos and code blocks. Links of the form x.com/<handle>/article/<id> open signed in or out; signed out, X shows no engagement counts, so those come back empty. Links of the form x.com/i/article/<id> open only for a signed-in account.

- Site: x.com
- Address: `reduck/x.com/get_article`
- Updated: 2026-10-06 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/get_article`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/get_article
```

## Input

- `url` (string, required): Link to the X Article: https://x.com/<handle>/article/<id> (opens signed in or out) or https://x.com/i/article/<id> (opens only for a signed-in account).

## Output

- `url` (string, required): Canonical link, https://x.com/<handle>/article/<tweet_id>, whichever link shape was passed.
- `text` (string, required): The body as plain text: each block's text, or a code block's markdown, separated by a blank line. Media are left out.
- `title` (string | null, required)
- `author` (object | null, required)
- `blocks` (array, required): The body in reading order, one entry per paragraph, heading, list item, quote or embed.
- `tweet_id` (string, required): Id of the post the article is published as; the id in the canonical link.
- `article_id` (string | null, required): Id of the article itself; the id in an x.com/i/article/<id> link.
- `published_at` (string | null, required): ISO 8601 time the article was first published.
- `likes` (integer | null, optional): null when signed out: X shows no counts to visitors.
- `views` (integer | null, optional): null when signed out or when X shows no view count.
- `quotes` (integer | null, optional): null when signed out.
- `replies` (integer | null, optional): null when signed out.
- `retweets` (integer | null, optional): Reposts without quotes. X's displayed repost count is retweets + quotes. null when signed out.
- `bookmarks` (integer | null, optional): null when signed out.
- `cover_image_url` (string | null, optional)

## FAQ

### What does "Read an X (Twitter) Article" do?

Read a long-form X (Twitter) Article from its link: title, author, publish date, cover image, engagement counts, and the full body in reading order, with its headings, lists, quotes, links, images, videos and code blocks. Links of the form x.com/<handle>/article/<id> open signed in or out; signed out, X shows no engagement counts, so those come back empty. Links of the form x.com/i/article/<id> open only for a signed-in account.

### How do I automatically read an X (Twitter) Article on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/get_article, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_article

### Is there a x.com API to read an X (Twitter) Article?

You do not need one. "Read an X (Twitter) Article" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns url, text, likes, title, views, author, blocks, quotes, replies, retweets, tweet_id, bookmarks, article_id, published_at, cover_image_url.

### Do I need to be logged in to x.com?

No. It only uses pages of x.com that are reachable without signing in.

### Does it change anything on x.com, or only read data?

It only reads. It looks things up on x.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/get_article, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_article

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/get_article
