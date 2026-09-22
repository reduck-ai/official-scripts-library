# Post tweet

Automatically post tweet on x.com. Post a tweet on X, with or without media. Attach one image (JPEG, PNG, GIF, WebP) or video (MP4) by link or as base64 bytes; a link the browser can reach works, including a file served from the machine running the browser, so a full-size photo or video needs no upload step. Returns the new tweet's id, url, author handle, text, and what was actually attached.

- Site: x.com
- Address: `reduck/x.com/post_tweet`
- Updated: 2026-09-03 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/post_tweet`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/post_tweet
```

## Input

- `text` (string, required): The tweet body text (≤280 chars, as X weighs it). Any @handle in the text is validated against a real, non-suspended X account before anything is posted — the run throws naming the bad handle if one doesn't resolve. Every call posts immediately and irreversibly in public, with no preview or confirmation step inside the script, so show the exact text and any media to the user and get their explicit approval for this specific content before running — approval from an earlier or unrelated message does not carry over.
- `media_url` (string, optional): Optional link to one image (JPEG, PNG, GIF, WebP) or video (MP4) to attach. The browser fetches it, so any host it can reach works, including a file served from the machine running the browser (python3 -m http.server 8765 --bind 127.0.0.1 → http://127.0.0.1:8765/pic.jpg). This is the route to use for a real photo or video: it has no size ceiling. The link must point at the file itself — a page about the file is refused before anything is published. Media is part of the published, irreversible content, so confirm it with the user before running, the same as the text.
- `media_path` (string, optional): Optional absolute path to an image or video on the machine running the browser. Attaching it directly only works on a browser that permits attaching local files this way, which an extension-paired browser refuses — so this only works on a local (reduck local / CLI) device; on any other device use media_url or media_base64. Confirm the exact file with the user before running.
- `media_base64` (string, optional): Optional image or video as base64 bytes, as an alternative to media_url. A data: prefix, line wrapping and base64url characters are all accepted. Suitable only for small files: arguments arriving over MCP are capped around 96KB of base64 (roughly a 72KB file) by the transport itself, which rejects the call before the script runs, and hand-transcribed base64 corrupts easily — generate it with a command (base64 -i pic.jpg | tr -d '\n') rather than typing it, or prefer media_url.
- `media_filename` (string, optional): Optional filename to present the attachment under (e.g. chart.png). Defaults to the name in media_url, or 'media' plus the extension matching the detected file type.

## Output

- `url` (string | null, required)
- `text` (string, required)
- `handle` (string | null, required)
- `tweet_id` (string | null, required)
- `media_count` (integer, required): Number of media attachments on the posted tweet (0 if text-only), read back from X's own response to the publish.
- `account_used` (string | null, required): handle of the logged-in account that performed the action, read from the account switcher UI (not assumed from input).
- `already_present` (boolean, required): true if a post with this exact text was already found on the account's own timeline before attempting to publish (duplicate-avoidance check); when true, publishing is skipped and tweet_id/url are null.
- `verified_on_page` (boolean, required): true if the script navigated to the new tweet's URL after publishing and confirmed the article is actually present.
- `media_type` (string | null, optional): The attachment's detected type (e.g. image/jpeg, video/mp4), or null on a text-only post.
- `media_bytes` (integer | null, optional): Size in bytes of the attached file as the browser decoded it, so a truncated payload is visible in the result. Null when no media was attached, or when it came from media_path.

## FAQ

### What does "Post tweet" do?

Post a tweet on X, with or without media. Attach one image (JPEG, PNG, GIF, WebP) or video (MP4) by link or as base64 bytes; a link the browser can reach works, including a file served from the machine running the browser, so a full-size photo or video needs no upload step. Returns the new tweet's id, url, author handle, text, and what was actually attached.

### How do I automatically post tweet on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/post_tweet, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/post_tweet

### Is there a x.com API to post tweet?

You do not need one. "Post tweet" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Required: text. Optional: media_url, media_path, media_base64, media_filename.

### What does it return?

It returns url, text, handle, tweet_id, media_type, media_bytes, media_count, account_used, already_present, verified_on_page.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It makes changes on x.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/post_tweet, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/post_tweet

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/post_tweet
