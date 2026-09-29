# Search Noota transcripts

Automatically search Noota transcripts on noota.io. Find who said what across your Noota meeting transcripts. A transcript line matches when it contains every word of the query, ignoring case and accents. For each match it returns the meeting, its date, the speaker, the start and end time in seconds, the line's text and a link to the meeting. Searches your 50 most recent meetings by default (up to 200), optionally only meetings whose title contains given text. It reports how many meetings were searched and how many have no transcript yet. Transcripts are Noota's speech-to-text, so names can be misheard (e.g. "Konto" for Qonto): search on the words as spoken. Read-only.

- Site: noota.io
- Address: `reduck/noota.io/search_transcripts`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/noota.io/search_transcripts`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/noota.io/search_transcripts
```

## Input

- `query` (string, required): Words to find. A transcript line matches when it contains every word (case- and accent-insensitive).
- `meeting` (string, optional): Optional: only search meetings whose title contains this text.
- `maxResults` (integer, optional)
- `maxMeetings` (integer, optional): Search at most this many of your most recent meetings.

## Output

- `count` (integer, required)
- `query` (string, required)
- `results` (array, required)
- `meetingsSearched` (integer, required): Meetings whose transcript was searched.
- `errors` (array, optional)
- `meetingsWithoutTranscript` (integer, optional): Meetings skipped because they have no transcript yet.

## FAQ

### What does "Search Noota transcripts" do?

Find who said what across your Noota meeting transcripts. A transcript line matches when it contains every word of the query, ignoring case and accents. For each match it returns the meeting, its date, the speaker, the start and end time in seconds, the line's text and a link to the meeting. Searches your 50 most recent meetings by default (up to 200), optionally only meetings whose title contains given text. It reports how many meetings were searched and how many have no transcript yet. Transcripts are Noota's speech-to-text, so names can be misheard (e.g. "Konto" for Qonto): search on the words as spoken. Read-only.

### How do I automatically search Noota transcripts on noota.io?

Ask an AI agent connected to Reduck to run reduck/noota.io/search_transcripts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/noota.io/search_transcripts

### Is there a noota.io API to search Noota transcripts?

You do not need one. "Search Noota transcripts" drives the real noota.io pages in a browser, so it works whether or not noota.io offers an API for this.

### What information do I need to provide?

Required: query. Optional: meeting, maxResults, maxMeetings.

### What does it return?

It returns count, query, errors, results, meetingsSearched, meetingsWithoutTranscript.

### Do I need to be logged in to noota.io?

Yes. It acts as you on noota.io: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the noota.io cookies saved by the Reduck extension.

### Does it change anything on noota.io, or only read data?

It only reads. It looks things up on noota.io and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/noota.io/search_transcripts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/noota.io/search_transcripts

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/noota.io/search_transcripts
