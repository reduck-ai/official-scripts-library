# Get YouTube video transcript

Automatically get YouTube video transcript on youtube.com. Fetch a YouTube video's caption transcript (auto-generated or uploaded) with per-segment timestamps. Returns available:false when the video has no captions in any language. Some runs fail when YouTube plays an ad before the video, roughly 1 in 3; the script already retries, so if it still fails, call it again later. The paired-extension browser is more reliable than the managed browser, where YouTube often shows a sign-in check and no transcript is returned.

- Site: youtube.com
- Address: `reduck/youtube.com/get_transcript`
- Updated: 2026-10-05 (v22)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/youtube.com/get_transcript`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/youtube.com/get_transcript
```

## Input

- `video_id` (string, required): YouTube video id, e.g. "jNQXAC9IVRw" (the v= parameter, or the last path segment of a youtu.be link)

## Output

- `segments` (array, required)
- `video_id` (string, required)
- `available` (boolean, required): false only when the video is playable but has no captions in any language. A video that does not exist, or is private / region-blocked / sign-in-gated, throws instead of reporting false.
- `language` (string | null, optional): Language code of the track actually returned. Deterministic: the video's default caption track.

## FAQ

### What does "Get YouTube video transcript" do?

Fetch a YouTube video's caption transcript (auto-generated or uploaded) with per-segment timestamps. Returns available:false when the video has no captions in any language. Some runs fail when YouTube plays an ad before the video, roughly 1 in 3; the script already retries, so if it still fails, call it again later. The paired-extension browser is more reliable than the managed browser, where YouTube often shows a sign-in check and no transcript is returned.

### How do I automatically get YouTube video transcript on youtube.com?

Ask an AI agent connected to Reduck to run reduck/youtube.com/get_transcript, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/youtube.com/get_transcript

### Is there a youtube.com API to get YouTube video transcript?

You do not need one. "Get YouTube video transcript" drives the real youtube.com pages in a browser, so it works whether or not youtube.com offers an API for this.

### What information do I need to provide?

Required: video_id.

### What does it return?

It returns language, segments, video_id, available.

### Do I need to be logged in to youtube.com?

No. It only uses pages of youtube.com that are reachable without signing in.

### Does it change anything on youtube.com, or only read data?

It only reads. It looks things up on youtube.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/youtube.com/get_transcript, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/youtube.com/get_transcript

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/youtube.com/get_transcript
