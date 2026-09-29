# Noota – Download meeting recording

Automatically download meeting recording on noota.io. Opens one of your Noota meetings by its exact title and returns a direct link to download the video recording, along with when that link expires.

- Site: noota.io
- Address: `reduck/noota.io/download_recording`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/noota.io/download_recording`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/noota.io/download_recording
```

## Input

- `title` (string, required): Exact title of the meeting, as shown in the Noota meetings list.

## Output

- `title` (string, required)
- `filename` (string | null, required)
- `expiresAt` (string | null, required)
- `downloadUrl` (string | null, required)

## FAQ

### What does "Noota – Download meeting recording" do?

Opens one of your Noota meetings by its exact title and returns a direct link to download the video recording, along with when that link expires.

### How do I automatically download meeting recording on noota.io?

Ask an AI agent connected to Reduck to run reduck/noota.io/download_recording, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/noota.io/download_recording

### Is there a noota.io API to download meeting recording?

You do not need one. "Noota – Download meeting recording" drives the real noota.io pages in a browser, so it works whether or not noota.io offers an API for this.

### What information do I need to provide?

Required: title.

### What does it return?

It returns title, filename, expiresAt, downloadUrl.

### Do I need to be logged in to noota.io?

Yes. It acts as you on noota.io: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the noota.io cookies saved by the Reduck extension.

### Does it change anything on noota.io, or only read data?

It only reads. It looks things up on noota.io and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/noota.io/download_recording, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/noota.io/download_recording

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/noota.io/download_recording
