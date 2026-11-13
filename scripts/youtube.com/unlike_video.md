# Unlike YouTube video

Automatically unlike YouTube video on youtube.com. Remove your like from a YouTube video — has no effect if it isn't currently liked.

- Site: youtube.com
- Address: `reduck/youtube.com/unlike_video`
- Updated: 2026-11-12 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/youtube.com/unlike_video`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/youtube.com/unlike_video
```

## Input

- `video` (string, required): A YouTube video URL (watch?v=, youtu.be/, /shorts/, /embed/) or a bare 11-char video id.
- `account` (string, optional): Email (or a distinctive part of it) of the signed-in Google account to act as, e.g. "you@example.com". Omit to use the browser's default account. When several accounts are signed in, name the intended one.

## Output

- `liked` (boolean, required): Always false on success - the video is no longer liked.
- `videoId` (string, required)
- `account` (string | null, optional): Email of the account the page used, when it could be read.
- `authuser` (integer | null, optional): Session index used; null when the browser default was used.
- `alreadyUnliked` (boolean, optional): true if the video was not liked to begin with (no click performed).

## FAQ

### What does "Unlike YouTube video" do?

Remove your like from a YouTube video — has no effect if it isn't currently liked.

### How do I automatically unlike YouTube video on youtube.com?

Ask an AI agent connected to Reduck to run reduck/youtube.com/unlike_video, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/youtube.com/unlike_video

### Is there a youtube.com API to unlike YouTube video?

You do not need one. "Unlike YouTube video" drives the real youtube.com pages in a browser, so it works whether or not youtube.com offers an API for this.

### What information do I need to provide?

Required: video. Optional: account.

### What does it return?

It returns liked, account, videoId, authuser, alreadyUnliked.

### Do I need to be logged in to youtube.com?

Yes. It acts as you on youtube.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the youtube.com cookies saved by the Reduck extension.

### Does it change anything on youtube.com, or only read data?

It makes changes on youtube.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/youtube.com/unlike_video, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/youtube.com/unlike_video

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/youtube.com/unlike_video
