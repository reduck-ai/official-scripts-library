# Get Instagram hashtag posts

Automatically get Instagram hashtag posts on instagram.com. Fetch the top posts for a hashtag. Returns how many posts carry the hashtag and the top-grid entries (code, url, user, like_count, comment_count, caption, thumbnail, media_type, taken_at). This is the Top preview Instagram renders first, not the full paginated Recent feed. Pass the tag without the leading #; it is matched the way Instagram spells it, so capitals are fine. Some hashtags have posts but no preview, because Instagram withholds the top grid for topics it restricts: the post list then comes back empty and restricted is true, so that case is distinguishable from a hashtag nobody has used. A hashtag with no posts at all is reported as such.

- Site: instagram.com
- Address: `reduck/instagram.com/get_hashtag_posts`
- Updated: 2026-09-03 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/get_hashtag_posts`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_hashtag_posts
```

## Input

- `tag` (string, required): Hashtag without the leading #, e.g. "nasa" or "spacex".

## Output

- `tag` (string, required): The hashtag as Instagram spells it (always lowercase).
- `posts` (array, required)
- `restricted` (boolean, required): True when Instagram withholds the top-post preview for this hashtag even though posts exist, so an empty posts list is not the same as an unused hashtag.
- `media_count` (integer | null, required)

## FAQ

### What does "Get Instagram hashtag posts" do?

Fetch the top posts for a hashtag. Returns how many posts carry the hashtag and the top-grid entries (code, url, user, like_count, comment_count, caption, thumbnail, media_type, taken_at). This is the Top preview Instagram renders first, not the full paginated Recent feed. Pass the tag without the leading #; it is matched the way Instagram spells it, so capitals are fine. Some hashtags have posts but no preview, because Instagram withholds the top grid for topics it restricts: the post list then comes back empty and restricted is true, so that case is distinguishable from a hashtag nobody has used. A hashtag with no posts at all is reported as such.

### How do I automatically get Instagram hashtag posts on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_hashtag_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_hashtag_posts

### Is there a instagram.com API to get Instagram hashtag posts?

You do not need one. "Get Instagram hashtag posts" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: tag.

### What does it return?

It returns tag, posts, restricted, media_count.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It only reads. It looks things up on instagram.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_hashtag_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_hashtag_posts

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/get_hashtag_posts
