# Get Instagram profile highlights

Automatically get Instagram profile highlights on instagram.com. List an Instagram user's Story Highlights by username (from get_profile). Returns each highlight's id, title and cover image, as the profile's highlights tray shows them; a profile with no highlights returns an empty list. This is the tray on the profile, not the story items inside each highlight. Fails with a clear error when the browser is not signed in to Instagram or the username does not exist.

- Site: instagram.com
- Address: `reduck/instagram.com/get_highlights`
- Updated: 2026-10-23 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/get_highlights`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_highlights
```

## Input

- `username` (string, required): Instagram username, without the @ (get_profile returns it).

## Output

- `username` (string, required)
- `highlights` (array, required)

## FAQ

### What does "Get Instagram profile highlights" do?

List an Instagram user's Story Highlights by username (from get_profile). Returns each highlight's id, title and cover image, as the profile's highlights tray shows them; a profile with no highlights returns an empty list. This is the tray on the profile, not the story items inside each highlight. Fails with a clear error when the browser is not signed in to Instagram or the username does not exist.

### How do I automatically get Instagram profile highlights on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_highlights, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_highlights

### Is there a instagram.com API to get Instagram profile highlights?

You do not need one. "Get Instagram profile highlights" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: username.

### What does it return?

It returns username, highlights.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

Unknown: its author has not declared whether it changes anything on instagram.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_highlights, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_highlights

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/get_highlights
