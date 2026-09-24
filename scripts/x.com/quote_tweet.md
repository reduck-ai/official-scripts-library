# Quote tweet

Automatically quote tweet on x.com. Quote-tweet a given tweet URL with your own commentary. Returns the new tweet's id, url, the quoted tweet id, and author handle.

- Site: x.com
- Address: `reduck/x.com/quote_tweet`
- Updated: 2026-09-22 (v17)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/quote_tweet`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/quote_tweet
```

## Input

- `text` (string, required): Your commentary on the quoted tweet (≤280 chars, as X weighs it — a URL counts as 23 regardless of length). If X's composer rejects the text, the script throws before publishing instead of hanging. Any @handle in the text is validated against a real, non-suspended X account before anything is posted — the run throws naming the bad handle if one doesn't resolve. Unless dry_run is set, every call posts immediately and irreversibly in public, with no preview or confirmation step inside the script, so show the exact tweet_url being quoted and this exact text (and any media) to the user and get their explicit approval for this specific content before running — approval from an earlier or unrelated message does not carry over.
- `tweet_url` (string, required): Full URL of the tweet to quote, e.g. https://x.com/handle/status/123. Confirm the exact URL with the user before running.
- `dry_run` (boolean, optional): When true, everything runs up to and including the attachment landing in the composer, then the run stops and publishes nothing — tweet_id and url come back null and already_present/verified_on_page are false. Use it to prove media attaches, or to rehearse a quote, without a public irreversible write.
- `media_url` (string, optional): Optional link to one image (JPEG, PNG, GIF, WebP) or video (MP4) to attach. The browser fetches it, so any host it can reach works, including a file served from the machine running the browser (python3 -m http.server 8765 --bind 127.0.0.1 → http://127.0.0.1:8765/pic.jpg). No size ceiling. The link must point at the file itself — a page about the file is refused before anything is published. Media is part of the published, irreversible content, so confirm it with the user before running, the same as the text.
- `attachment` (string, optional): One image or video to attach, bound through the platform's own file channel and handed straight to the composer's file input. Carries the bytes outside the argument payload, so unlike media_base64 it is not limited by the request size, and unlike media_path it needs no special browser permission. Pass at most one of attachment / media_url / media_base64 / media_path.
- `media_path` (string, optional): Optional absolute path to an image or video on the machine running the browser. Attaching it directly only works on a browser that permits it, which an extension-paired browser refuses — prefer the `attachment` input, which works on every device. Confirm the exact file with the user before running.
- `media_base64` (string, optional): Optional image or video as base64 bytes. A data: prefix, line wrapping and base64url characters are all accepted. Suitable only for small files: arguments arriving over MCP are capped around 96KB of base64 by the transport itself. Prefer the `attachment` input, which has no such cap.
- `media_filename` (string, optional): Optional filename to present the attachment under (e.g. chart.png). Defaults to the name in media_url, or 'media' plus the extension matching the detected file type. Not used with the `attachment` input, which carries its own name.

## Output

- `url` (string | null, required)
- `text` (string, required)
- `handle` (string | null, required)
- `quoted` (string | null, required): id of the quoted tweet
- `tweet_id` (string | null, required)
- `account_used` (string | null, required): handle of the logged-in account that performed the action, read from the account switcher UI (not assumed from input).
- `already_present` (boolean, required): true if this text already appears on the most recent page of the account's own posts (~20, read from X's own profile-timeline payload), so publishing was skipped and tweet_id/url are null. Comparison strips URLs and emoji from both sides, since the submitted text carries the original link while X stores a shortened t.co one. A duplicate older than that first page is not detected here and surfaces instead as X's own "Status is a duplicate. (187)" refusal.
- `verified_on_page` (boolean, required): true if the script navigated to the new tweet's URL after publishing and confirmed the article is actually present.
- `dry_run` (boolean, optional): true if this run stopped before publishing because dry_run was set. When true the attachment, if any, was confirmed present in the composer and then discarded.
- `media_type` (string | null, optional): The attachment's detected type (e.g. image/jpeg, video/mp4), or null on a text-only quote.
- `media_bytes` (integer | null, optional): Size in bytes of the attached file as the browser decoded it, so a truncated payload is visible in the result. Null when no media was attached, or when it came from media_path.
- `media_count` (integer, optional): Number of media attachments on the posted quote (0 if text-only).

## FAQ

### What does "Quote tweet" do?

Quote-tweet a given tweet URL with your own commentary. Returns the new tweet's id, url, the quoted tweet id, and author handle.

### How do I automatically quote tweet on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/quote_tweet, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/quote_tweet

### Is there a x.com API to quote tweet?

You do not need one. "Quote tweet" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Required: tweet_url, text. Optional: dry_run, media_url, attachment, media_path, media_base64, media_filename.

### What does it return?

It returns url, text, handle, quoted, dry_run, tweet_id, media_type, media_bytes, media_count, account_used, already_present, verified_on_page.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It makes changes on x.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/quote_tweet, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/quote_tweet

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/quote_tweet
