# Like YouTube video

Automatically like YouTube video on youtube.com. Like a YouTube video — has no effect if it's already liked.

- Site: youtube.com
- Address: `reduck/youtube.com/like_video`
- Updated: 2026-08-14 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/youtube.com/like_video`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/youtube.com/like_video
```

## Input

- `video` (string, required): A YouTube video URL (watch?v=, youtu.be/, /shorts/, /embed/) or a bare 11-char video id.

## Output

- `liked` (boolean, required): Always true on success — the video is in the liked state.
- `videoId` (string, required)
- `alreadyLiked` (boolean, optional): true if the video was already liked (no click performed).

## FAQ

### What does "Like YouTube video" do?

Like a YouTube video — has no effect if it's already liked.

### How do I automatically like YouTube video on youtube.com?

Ask an AI agent connected to Reduck to run reduck/youtube.com/like_video, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/youtube.com/like_video

### Is there a youtube.com API to like YouTube video?

You do not need one. "Like YouTube video" drives the real youtube.com pages in a browser, so it works whether or not youtube.com offers an API for this.

### What information do I need to provide?

Required: video.

### What does it return?

It returns liked, videoId, alreadyLiked.

### Do I need to be logged in to youtube.com?

Yes. It acts as you on youtube.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the youtube.com cookies saved by the Reduck extension.

### Does it change anything on youtube.com, or only read data?

It makes changes on youtube.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/youtube.com/like_video, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/youtube.com/like_video

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/youtube.com/like_video
