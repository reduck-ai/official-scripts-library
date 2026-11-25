# Get Instagram user stories

Automatically get Instagram user stories on instagram.com. Get an Instagram account's currently live story items by username (get_profile returns it). Returns the username, the numeric user_id and items (id, taken_at, expiring_at, media_type 1=photo/2=video, image_url, video_url). Reading does not mark the stories as viewed. Empty items means no live story (they expire after 24 hours) or none visible to you. An unknown username is an error.

- Site: instagram.com
- Address: `reduck/instagram.com/get_stories`
- Updated: 2026-11-24 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/get_stories`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_stories
```

## Input

- `username` (string, required): Instagram username, with or without @ (get_profile returns it).

## Output

- `items` (array, required)
- `username` (string, required)
- `user_id` (string | null, optional): Numeric user id, from the story data; null when nothing is live.

## FAQ

### What does "Get Instagram user stories" do?

Get an Instagram account's currently live story items by username (get_profile returns it). Returns the username, the numeric user_id and items (id, taken_at, expiring_at, media_type 1=photo/2=video, image_url, video_url). Reading does not mark the stories as viewed. Empty items means no live story (they expire after 24 hours) or none visible to you. An unknown username is an error.

### How do I automatically get Instagram user stories on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_stories, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_stories

### Is there a instagram.com API to get Instagram user stories?

You do not need one. "Get Instagram user stories" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: username.

### What does it return?

It returns items, user_id, username.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for instagram.com.

### Does it change anything on instagram.com, or only read data?

It only reads. It looks things up on instagram.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_stories, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_stories

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/get_stories
