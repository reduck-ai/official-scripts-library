# Get 14-day weather forecast

Automatically get 14-day weather forecast on meteoblue.com. 14-day weather forecast for any city worldwide (meteoblue): per-day condition, min/max temp, predictability. Optional date filter (YYYY-MM-DD).

- Site: meteoblue.com
- Address: `reduck/meteoblue.com/get_14day_forecast`
- Updated: 2026-07-20 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/meteoblue.com/get_14day_forecast`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/meteoblue.com/get_14day_forecast
```

## Input

- `location` (string, required): City name as a human types it, e.g. "Luçon", "Oakland", "Marina di Andora". Resolved via meteoblue's own location search (first/best match, ranked by relevance).
- `date` (string, optional): Optional ISO date (YYYY-MM-DD). When given, `days` contains only that day — empty array if the date is outside the 14-day window (not an error).

## Output

- `days` (array, required): One entry per forecast day (14 unless filtered by the date arg; empty if date out of window)
- `location` (object, required)

## FAQ

### What does "Get 14-day weather forecast" do?

14-day weather forecast for any city worldwide (meteoblue): per-day condition, min/max temp, predictability. Optional date filter (YYYY-MM-DD).

### How do I automatically get 14-day weather forecast on meteoblue.com?

Ask an AI agent connected to Reduck to run reduck/meteoblue.com/get_14day_forecast, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/meteoblue.com/get_14day_forecast

### Is there a meteoblue.com API to get 14-day weather forecast?

You do not need one. "Get 14-day weather forecast" drives the real meteoblue.com pages in a browser, so it works whether or not meteoblue.com offers an API for this.

### What information do I need to provide?

Required: location. Optional: date.

### What does it return?

It returns days, location.

### Do I need to be logged in to meteoblue.com?

No. It only uses pages of meteoblue.com that are reachable without signing in.

### Does it change anything on meteoblue.com, or only read data?

Unknown: its author has not declared whether it changes anything on meteoblue.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/meteoblue.com/get_14day_forecast, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/meteoblue.com/get_14day_forecast

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/meteoblue.com/get_14day_forecast
