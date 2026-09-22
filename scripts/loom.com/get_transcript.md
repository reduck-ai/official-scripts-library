# Get Loom video transcript

Automatically get Loom video transcript on loom.com. Fetch the full transcript of a Loom video from its share URL (or bare 32-char id). Returns title, owner, duration, language, timestamped segments, and the joined plain text. Works anonymously on link-shared videos; password-protected or private videos fail loudly, and videos without a transcript return an empty segments list.

- Site: loom.com
- Address: `reduck/loom.com/get_transcript`
- Updated: 2026-08-18 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/loom.com/get_transcript`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/loom.com/get_transcript
```

## Input

- `url` (string, required): Loom share URL (https://www.loom.com/share/<32-hex-id>, extra query params OK) or the bare 32-char video id

## Output

- `text` (string, required): All segments joined with newlines
- `videoId` (string, required)
- `segments` (array, required)
- `title` (string | null, optional)
- `language` (string | null, optional)
- `createdAt` (string | null, optional)
- `ownerName` (string | null, optional)
- `durationSeconds` (number | null, optional)
- `transcriptionStatus` (string | null, optional): Loom-side status, e.g. "success"; null when the video has no transcript

## FAQ

### What does "Get Loom video transcript" do?

Fetch the full transcript of a Loom video from its share URL (or bare 32-char id). Returns title, owner, duration, language, timestamped segments, and the joined plain text. Works anonymously on link-shared videos; password-protected or private videos fail loudly, and videos without a transcript return an empty segments list.

### How do I automatically get Loom video transcript on loom.com?

Ask an AI agent connected to Reduck to run reduck/loom.com/get_transcript, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/loom.com/get_transcript

### Is there a loom.com API to get Loom video transcript?

You do not need one. "Get Loom video transcript" drives the real loom.com pages in a browser, so it works whether or not loom.com offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns text, title, videoId, language, segments, createdAt, ownerName, durationSeconds, transcriptionStatus.

### Do I need to be logged in to loom.com?

No. It only uses pages of loom.com that are reachable without signing in.

### Does it change anything on loom.com, or only read data?

It only reads. It looks things up on loom.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/loom.com/get_transcript, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/loom.com/get_transcript

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/loom.com/get_transcript
