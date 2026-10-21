# Get meteoblue 14-day weather forecast

Automatically get meteoblue 14-day weather forecast on meteoblue.com. 14-day weather forecast from meteoblue for one place, given its meteoblue location url (from meteoblue.com/search_locations): per day, the date, weekday, sky condition, min/max temperature in °C and meteoblue's predictability. A url meteoblue does not serve fails with that.

- Site: meteoblue.com
- Address: `reduck/meteoblue.com/get_14day_forecast`
- Updated: 2026-10-20 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/meteoblue.com/get_14day_forecast`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/meteoblue.com/get_14day_forecast
```

## Input

- `url` (string, optional): Same as location, under the name meteoblue.com/search_locations returns it. Pass one of location or url.
- `location` (string, optional): meteoblue location url, e.g. "paris_france_2988507": get it from meteoblue.com/search_locations.

## Output

- `days` (array, required): One entry per forecast day, as the 14-day table shows them.
- `location` (object, required)

## FAQ

### What does "Get meteoblue 14-day weather forecast" do?

14-day weather forecast from meteoblue for one place, given its meteoblue location url (from meteoblue.com/search_locations): per day, the date, weekday, sky condition, min/max temperature in °C and meteoblue's predictability. A url meteoblue does not serve fails with that.

### How do I automatically get meteoblue 14-day weather forecast on meteoblue.com?

Ask an AI agent connected to Reduck to run reduck/meteoblue.com/get_14day_forecast, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/meteoblue.com/get_14day_forecast

### Is there a meteoblue.com API to get meteoblue 14-day weather forecast?

You do not need one. "Get meteoblue 14-day weather forecast" drives the real meteoblue.com pages in a browser, so it works whether or not meteoblue.com offers an API for this.

### What information do I need to provide?

Optional: url, location.

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
