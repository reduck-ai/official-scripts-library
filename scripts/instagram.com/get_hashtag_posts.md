# Get Instagram hashtag posts

Automatically get Instagram hashtag posts on instagram.com. Get the top posts Instagram shows for a hashtag: code, url, user, like and comment counts, caption, thumbnail, media type and posting time for each. This is the first page Instagram shows for the hashtag, not its full feed. Pass the tag without the leading #; capitals are fine. A hashtag nobody has used returns an empty post list. Instagram no longer shows how many posts carry a hashtag or whether it withholds some, so media_count and restricted are always null.

- Site: instagram.com
- Address: `reduck/instagram.com/get_hashtag_posts`
- Updated: 2026-11-24 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/get_hashtag_posts`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_hashtag_posts
```

## Input

- `tag` (string, required): Hashtag without the leading #, e.g. "nasa" or "spacex".

## Output

- `tag` (string, required): The hashtag as searched, lowercase.
- `posts` (array, required)
- `restricted` (boolean | null, required): Always null: Instagram no longer says when it withholds a hashtag's posts.
- `media_count` (integer | null, required): Always null: Instagram no longer shows how many posts carry the hashtag.

## FAQ

### What does "Get Instagram hashtag posts" do?

Get the top posts Instagram shows for a hashtag: code, url, user, like and comment counts, caption, thumbnail, media type and posting time for each. This is the first page Instagram shows for the hashtag, not its full feed. Pass the tag without the leading #; capitals are fine. A hashtag nobody has used returns an empty post list. Instagram no longer shows how many posts carry a hashtag or whether it withholds some, so media_count and restricted are always null.

### How do I automatically get Instagram hashtag posts on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_hashtag_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_hashtag_posts

### Is there a instagram.com API to get Instagram hashtag posts?

You do not need one. "Get Instagram hashtag posts" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: tag.

### What does it return?

It returns tag, posts, restricted, media_count.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for instagram.com.

### Does it change anything on instagram.com, or only read data?

It only reads. It looks things up on instagram.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_hashtag_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_hashtag_posts

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/get_hashtag_posts
