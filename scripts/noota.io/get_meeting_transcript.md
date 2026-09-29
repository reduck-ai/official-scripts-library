# Noota – Get meeting transcript

Automatically get meeting transcript on noota.io. Opens one of your Noota meetings by its exact title and returns the full transcript, in order, with each line's speaker and text.

- Site: noota.io
- Address: `reduck/noota.io/get_meeting_transcript`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/noota.io/get_meeting_transcript`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/noota.io/get_meeting_transcript
```

## Input

- `title` (string, required): Exact title of the meeting, as shown in the Noota meetings list.

## Output

- `title` (string, required)
- `shareUrl` (string, required)
- `transcript` (array, required)

## FAQ

### What does "Noota – Get meeting transcript" do?

Opens one of your Noota meetings by its exact title and returns the full transcript, in order, with each line's speaker and text.

### How do I automatically get meeting transcript on noota.io?

Ask an AI agent connected to Reduck to run reduck/noota.io/get_meeting_transcript, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/noota.io/get_meeting_transcript

### Is there a noota.io API to get meeting transcript?

You do not need one. "Noota – Get meeting transcript" drives the real noota.io pages in a browser, so it works whether or not noota.io offers an API for this.

### What information do I need to provide?

Required: title.

### What does it return?

It returns title, shareUrl, transcript.

### Do I need to be logged in to noota.io?

Yes. It acts as you on noota.io: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the noota.io cookies saved by the Reduck extension.

### Does it change anything on noota.io, or only read data?

It only reads. It looks things up on noota.io and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/noota.io/get_meeting_transcript, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/noota.io/get_meeting_transcript

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/noota.io/get_meeting_transcript
