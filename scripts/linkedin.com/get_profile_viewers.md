# Get LinkedIn profile viewers

Automatically get LinkedIn profile viewers on linkedin.com. List who viewed your LinkedIn profile: the total for the period LinkedIn shows, and each viewer it shows in detail (name, headline, profile link and when they viewed, or a teaser for a hidden viewer). A free account sees only a few viewers in detail; complete is false when LinkedIn holds more than returned.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_profile_viewers`
- Updated: 2026-11-10 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_profile_viewers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_profile_viewers
```

## Input

- `limit` (integer, optional): Most viewers to return.

## Output

- `total` (integer | null, required): Profile viewers in the period LinkedIn shows (past 90 days).
- `viewers` (array, required)
- `complete` (boolean, required): false when LinkedIn has more viewers than returned (limit reached, or a list only Premium can open).
- `shownCount` (integer, required)
- `privateModeCount` (integer | null, required): Viewers counted only in aggregate as private mode; null when LinkedIn does not show that count.

## FAQ

### What does "Get LinkedIn profile viewers" do?

List who viewed your LinkedIn profile: the total for the period LinkedIn shows, and each viewer it shows in detail (name, headline, profile link and when they viewed, or a teaser for a hidden viewer). A free account sees only a few viewers in detail; complete is false when LinkedIn holds more than returned.

### How do I automatically get LinkedIn profile viewers on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_profile_viewers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_profile_viewers

### Is there a linkedin.com API to get LinkedIn profile viewers?

You do not need one. "Get LinkedIn profile viewers" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Optional: limit.

### What does it return?

It returns total, viewers, complete, shownCount, privateModeCount.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_profile_viewers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_profile_viewers

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_profile_viewers
