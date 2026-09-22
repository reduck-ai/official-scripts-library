# List the signed-in account's saved Instagram posts

Automatically list the signed-in account's saved Instagram posts on instagram.com. List the posts the signed-in Instagram account has saved (bookmarked), from the "All posts" saved collection. Returns each post's code (the /p/&lt;code&gt;/ URL segment), owner username, caption text, like count, and taken-at timestamp. Only you can see what you've saved — this is your own private list.

- Site: instagram.com
- Address: `reduck/instagram.com/get_saved_posts`
- Updated: 2026-09-21 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/get_saved_posts`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_saved_posts
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `posts` (array, required)
- `moreAvailable` (boolean, required)

## FAQ

### What does "List the signed-in account's saved Instagram posts" do?

List the posts the signed-in Instagram account has saved (bookmarked), from the "All posts" saved collection. Returns each post's code (the /p/&lt;code&gt;/ URL segment), owner username, caption text, like count, and taken-at timestamp. Only you can see what you've saved — this is your own private list.

### How do I automatically list the signed-in account's saved Instagram posts on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_saved_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_saved_posts

### Is there a instagram.com API to list the signed-in account's saved Instagram posts?

You do not need one. "List the signed-in account's saved Instagram posts" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, posts, moreAvailable.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It only reads. It looks things up on instagram.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_saved_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_saved_posts

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/get_saved_posts
