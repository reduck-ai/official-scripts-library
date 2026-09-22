# Create Instagram reel

Automatically create Instagram reel on instagram.com. Publish an Instagram reel from a video URL (fetched in-browser, max 25MB) or a local mp4 file (video_path, no size limit, requires a CLI-run device). Accepts the default cover and confirms the reel was shared, including the caption that was actually applied.

- Site: instagram.com
- Address: `reduck/instagram.com/create_reel`
- Updated: 2026-09-22 (v20)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/create_reel`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/create_reel
```

## Input

- `caption` (string, optional): Reel caption; empty for none. Max 2200 chars.
- `dry_run` (boolean, optional): When true, the whole flow runs — the video is fetched and attached, the crop and edit steps are passed, the cover is accepted and the caption typed — and then the run stops on the step before Share. Nothing is published: shared comes back false, code/url are null and dry_run is true. Use it to verify a video and caption are accepted without spending a real, irreversible public reel.
- `video_url` (string, optional): Direct URL of the mp4 to post as a reel; fetched by the browser and capped at 25MB because the bytes cross the browser boundary in one piece. To post a local file, serve it over localhost (e.g. `python3 -m http.server 8765 --bind 127.0.0.1` in its directory) and pass that URL, or use the `attachment` input, which has no such cap.
- `attachment` (string, optional): The mp4 to post, bound through the platform's own file channel and handed straight to the composer's file input. Preferred over the other two: it carries the bytes outside the argument payload, is not subject to the 25MB video_url ceiling, and needs no special browser permission the way video_path does.
- `video_path` (string, optional): Path to a local mp4 on the machine running the browser, attached directly with no size limit. Only works on a device whose browser permits attaching local files directly; an extension-paired browser refuses it. Prefer the `attachment` input, which works on every device. Absolute paths only. Takes precedence over video_url.

## Output

- `url` (string | null, required): Permalink of the new reel. Null on a dry run, where nothing was published.
- `shared` (boolean, required): True when the reel was actually published. Always false on a dry run.
- `caption_applied` (boolean, required): True when a caption was requested and Instagram recorded it; false when one was requested but the published reel carries none. Always true when no caption was requested. Always false on a dry run, where Instagram recorded nothing.
- `pk` (string | null, optional): Media pk. Null on a dry run.
- `code` (string | null, optional): Shortcode of the new reel. Null on a dry run, where nothing was published.
- `caption` (string, optional): The caption Instagram actually recorded on the published reel (read back after publish), NOT an echo of the input. Empty when none was requested, none landed, or the run was a dry run.
- `dry_run` (boolean, optional): True when this run stopped before Share and published nothing. The video was still attached and the caption still typed — only the final publish was skipped.
- `video_bytes` (number | null, optional): Size in bytes of the video injected into the composer. null for video_path, where the browser opens the file itself and the bytes never cross the driver boundary.

## FAQ

### What does "Create Instagram reel" do?

Publish an Instagram reel from a video URL (fetched in-browser, max 25MB) or a local mp4 file (video_path, no size limit, requires a CLI-run device). Accepts the default cover and confirms the reel was shared, including the caption that was actually applied.

### How do I automatically create Instagram reel on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/create_reel, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/create_reel

### Is there a instagram.com API to create Instagram reel?

You do not need one. "Create Instagram reel" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Optional: caption, dry_run, video_url, attachment, video_path.

### What does it return?

It returns pk, url, code, shared, caption, dry_run, video_bytes, caption_applied.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It makes changes on instagram.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/create_reel, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/create_reel

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/create_reel
