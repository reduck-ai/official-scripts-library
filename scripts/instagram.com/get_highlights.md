# Get Instagram profile highlights

Automatically get Instagram profile highlights on instagram.com. List an Instagram user's Story Highlights by their numeric user_id (from get_profile). Returns each highlight's id, title, media_count, cover_image, created_at, and updated_at. This is the highlights tray on the profile, not the individual story items inside each highlight.

- Site: instagram.com
- Address: `reduck/instagram.com/get_highlights`
- Updated: 2026-09-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/get_highlights`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_highlights
```

## Input

- `user_id` (string, required): Numeric user id (get_profile returns it as user_id).

## Output

- `user_id` (string, required)
- `highlights` (array, required)

## FAQ

### What does "Get Instagram profile highlights" do?

List an Instagram user's Story Highlights by their numeric user_id (from get_profile). Returns each highlight's id, title, media_count, cover_image, created_at, and updated_at. This is the highlights tray on the profile, not the individual story items inside each highlight.

### How do I automatically get Instagram profile highlights on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_highlights, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_highlights

### Is there a instagram.com API to get Instagram profile highlights?

You do not need one. "Get Instagram profile highlights" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: user_id.

### What does it return?

It returns user_id, highlights.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

Unknown: its author has not declared whether it changes anything on instagram.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_highlights, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_highlights

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/get_highlights
