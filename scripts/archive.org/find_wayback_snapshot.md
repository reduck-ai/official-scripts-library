# Find closest Wayback Machine snapshot

Automatically find closest Wayback Machine snapshot on archive.org. Find the Wayback Machine capture of a web page closest to a given date (or the latest one when no date is given). Returns the snapshot URL, its exact timestamp and HTTP status, or available false when the page was never archived.

- Site: archive.org
- Address: `reduck/archive.org/find_wayback_snapshot`
- Updated: 2026-11-19 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/archive.org/find_wayback_snapshot`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/archive.org/find_wayback_snapshot
```

## Input

- `url` (string, required): The page to look up, e.g. 'example.com/about'.
- `timestamp` (string, optional): Target date as YYYY, YYYYMMDD or YYYYMMDDhhmmss. Omit for the most recent capture.

## Output

- `url` (string, required)
- `available` (boolean, required)
- `status` (string | null, optional)
- `timestamp` (string | null, optional)
- `snapshot_url` (string | null, optional)

## FAQ

### What does "Find closest Wayback Machine snapshot" do?

Find the Wayback Machine capture of a web page closest to a given date (or the latest one when no date is given). Returns the snapshot URL, its exact timestamp and HTTP status, or available false when the page was never archived.

### How do I automatically find closest Wayback Machine snapshot on archive.org?

Ask an AI agent connected to Reduck to run reduck/archive.org/find_wayback_snapshot, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/archive.org/find_wayback_snapshot

### Is there a archive.org API to find closest Wayback Machine snapshot?

You do not need one. "Find closest Wayback Machine snapshot" drives the real archive.org pages in a browser, so it works whether or not archive.org offers an API for this.

### What information do I need to provide?

Required: url. Optional: timestamp.

### What does it return?

It returns url, status, available, timestamp, snapshot_url.

### Do I need to be logged in to archive.org?

No. It only uses pages of archive.org that are reachable without signing in.

### Does it change anything on archive.org, or only read data?

It only reads. It looks things up on archive.org and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/archive.org/find_wayback_snapshot, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/archive.org/find_wayback_snapshot

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/archive.org/find_wayback_snapshot
