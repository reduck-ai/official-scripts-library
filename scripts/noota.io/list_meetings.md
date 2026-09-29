# List Noota meetings

Automatically list Noota meetings on noota.io. List the meetings recorded in the signed-in Noota account, newest first: id, title, recording date, duration in seconds, processing status (e.g. Transcrit = transcribed), how it was captured (import, meeting bot…), owner, whether it is private, teamspace or shared with you, and a link to open it. Optionally filter by title text and cap the count. Only real meetings are returned; the sample meetings Noota shows new accounts are left out. The meeting id works with the other Noota scripts. Read-only.

- Site: noota.io
- Address: `reduck/noota.io/list_meetings`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/noota.io/list_meetings`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/noota.io/list_meetings
```

## Input

- `limit` (integer, optional)
- `query` (string, optional): Optional: only meetings whose title contains this text (case-insensitive).

## Output

- `count` (integer, required): Matching meetings before limit.
- `meetings` (array, required)

## FAQ

### What does "List Noota meetings" do?

List the meetings recorded in the signed-in Noota account, newest first: id, title, recording date, duration in seconds, processing status (e.g. Transcrit = transcribed), how it was captured (import, meeting bot…), owner, whether it is private, teamspace or shared with you, and a link to open it. Optionally filter by title text and cap the count. Only real meetings are returned; the sample meetings Noota shows new accounts are left out. The meeting id works with the other Noota scripts. Read-only.

### How do I automatically list Noota meetings on noota.io?

Ask an AI agent connected to Reduck to run reduck/noota.io/list_meetings, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/noota.io/list_meetings

### Is there a noota.io API to list Noota meetings?

You do not need one. "List Noota meetings" drives the real noota.io pages in a browser, so it works whether or not noota.io offers an API for this.

### What information do I need to provide?

Optional: limit, query.

### What does it return?

It returns count, meetings.

### Do I need to be logged in to noota.io?

Yes. It acts as you on noota.io: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the noota.io cookies saved by the Reduck extension.

### Does it change anything on noota.io, or only read data?

It only reads. It looks things up on noota.io and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/noota.io/list_meetings, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/noota.io/list_meetings

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/noota.io/list_meetings
