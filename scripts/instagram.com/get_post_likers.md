# Get Instagram post likers

Automatically get Instagram post likers on instagram.com. Fetch the accounts that liked an Instagram post or reel by shortcode. Returns like_count, available_count (how many liker entries Instagram exposed in this preview — its own cap, not the full like_count for popular posts), and likers (username, full_name, is_private, is_verified, following, followed_by, profile_pic_url).

- Site: instagram.com
- Address: `reduck/instagram.com/get_post_likers`
- Updated: 2026-09-03 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/get_post_likers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_post_likers
```

## Input

- `code` (string, required): Post shortcode, e.g. the X in instagram.com/p/X/
- `count` (integer, optional): Max likers to return

## Output

- `code` (string, required)
- `likers` (array, required)
- `url` (string, optional)
- `like_count` (integer | null, optional)
- `available_count` (integer, optional): How many liker entries Instagram exposed in this preview response — its own cap, not the same as like_count

## FAQ

### What does "Get Instagram post likers" do?

Fetch the accounts that liked an Instagram post or reel by shortcode. Returns like_count, available_count (how many liker entries Instagram exposed in this preview — its own cap, not the full like_count for popular posts), and likers (username, full_name, is_private, is_verified, following, followed_by, profile_pic_url).

### How do I automatically get Instagram post likers on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_post_likers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_post_likers

### Is there a instagram.com API to get Instagram post likers?

You do not need one. "Get Instagram post likers" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: code. Optional: count.

### What does it return?

It returns url, code, likers, like_count, available_count.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It only reads. It looks things up on instagram.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_post_likers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_post_likers

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/get_post_likers
