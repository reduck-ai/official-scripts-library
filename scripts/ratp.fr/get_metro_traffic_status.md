# Get RATP Paris metro traffic status per line

Automatically get RATP Paris metro traffic status per line on ratp.fr. Current traffic status of every line on the RATP metro traffic page (metro 1 to 14, 3B and 7B, plus Orlyval and the Montmartre funicular): normal, disrupted, or planned works. Returns one row per line, in the page's order, with the link to its details. No login needed. Read-only.

- Site: ratp.fr
- Address: `reduck/ratp.fr/get_metro_traffic_status`
- Updated: 2026-11-17 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ratp.fr/get_metro_traffic_status`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ratp.fr/get_metro_traffic_status
```

## Input

It takes no input.

## Output

- `as_of` (string | null, required): Time of day (Paris) the RATP page gives for this bulletin, HH:MM.
- `lines` (array, required)

## FAQ

### What does "Get RATP Paris metro traffic status per line" do?

Current traffic status of every line on the RATP metro traffic page (metro 1 to 14, 3B and 7B, plus Orlyval and the Montmartre funicular): normal, disrupted, or planned works. Returns one row per line, in the page's order, with the link to its details. No login needed. Read-only.

### How do I automatically get RATP Paris metro traffic status per line on ratp.fr?

Ask an AI agent connected to Reduck to run reduck/ratp.fr/get_metro_traffic_status, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ratp.fr/get_metro_traffic_status

### Is there a ratp.fr API to get RATP Paris metro traffic status per line?

You do not need one. "Get RATP Paris metro traffic status per line" drives the real ratp.fr pages in a browser, so it works whether or not ratp.fr offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns as_of, lines.

### Do I need to be logged in to ratp.fr?

No. It only uses pages of ratp.fr that are reachable without signing in.

### Does it change anything on ratp.fr, or only read data?

It only reads. It looks things up on ratp.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ratp.fr/get_metro_traffic_status, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ratp.fr/get_metro_traffic_status

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/ratp.fr/get_metro_traffic_status
