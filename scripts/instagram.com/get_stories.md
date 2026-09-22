# Get Instagram user stories

Automatically get Instagram user stories on instagram.com. Fetch a user's currently-active story items by their numeric user_id (from get_profile). Returns username and items (id, taken_at, expiring_at, media_type 1=photo/2=video, image_url, video_url). Empty items = no active story (they expire after 24h) or the account's stories aren't visible to you.

- Site: instagram.com
- Address: `reduck/instagram.com/get_stories`
- Updated: 2026-09-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/get_stories`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_stories
```

## Input

- `user_id` (string, required): Numeric user id (get_profile returns it as user_id).

## Output

- `items` (array, required)
- `user_id` (string, required)
- `username` (string | null, optional)

## FAQ

### What does "Get Instagram user stories" do?

Fetch a user's currently-active story items by their numeric user_id (from get_profile). Returns username and items (id, taken_at, expiring_at, media_type 1=photo/2=video, image_url, video_url). Empty items = no active story (they expire after 24h) or the account's stories aren't visible to you.

### How do I automatically get Instagram user stories on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_stories, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_stories

### Is there a instagram.com API to get Instagram user stories?

You do not need one. "Get Instagram user stories" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: user_id.

### What does it return?

It returns items, user_id, username.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

Unknown: its author has not declared whether it changes anything on instagram.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_stories, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_stories

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/get_stories
