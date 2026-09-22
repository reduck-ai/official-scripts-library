# Get profile viewers

Automatically get profile viewers on linkedin.com. List who viewed your LinkedIn profile (linkedin.com/analytics/profile-views). Returns the individually-shown viewers: named ones (name, headline, degree, publicId, profileUrl, mutualConnections) and semi-anonymized private ones (occupation/industry/geo teaser only, no name), plus viewedAgo per entry, the aggregate privateModeCount (fully-hidden viewers only counted, not shown), and the total profile-viewers metric for the window. Works across English, French, German, Spanish, and Italian account UI language; other languages may not resolve the total-viewers, mutual-connections, or private-mode counts correctly. The full 90-day list needs LinkedIn Premium (free tier shows only the last few).

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_profile_viewers`
- Updated: 2026-09-03 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_profile_viewers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_profile_viewers
```

## Input

- `limit` (integer, optional): Cap how many individually-shown viewers to load & return (stops scrolling early). Omit to return all shown viewers. Does not affect privateModeCount/total.

## Output

- `total` (integer | null, required): Profile-viewers count for the selected window (top metric).
- `viewers` (array, required)
- `shownCount` (integer, required): Number of individually-listed viewers returned.
- `privateModeCount` (integer | null, required): Viewers shown only as an aggregate 'N LinkedIn members viewed in Private mode' (0 if none, unless the account's UI language falls outside en/fr/de/es/it, in which case it's a best-effort match that may under-detect). Null when a `limit` stopped scrolling before the bottom row, where this count lives.

## FAQ

### What does "Get profile viewers" do?

List who viewed your LinkedIn profile (linkedin.com/analytics/profile-views). Returns the individually-shown viewers: named ones (name, headline, degree, publicId, profileUrl, mutualConnections) and semi-anonymized private ones (occupation/industry/geo teaser only, no name), plus viewedAgo per entry, the aggregate privateModeCount (fully-hidden viewers only counted, not shown), and the total profile-viewers metric for the window. Works across English, French, German, Spanish, and Italian account UI language; other languages may not resolve the total-viewers, mutual-connections, or private-mode counts correctly. The full 90-day list needs LinkedIn Premium (free tier shows only the last few).

### How do I automatically get profile viewers on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_profile_viewers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_profile_viewers

### Is there a linkedin.com API to get profile viewers?

You do not need one. "Get profile viewers" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Optional: limit.

### What does it return?

It returns total, viewers, shownCount, privateModeCount.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_profile_viewers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_profile_viewers

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_profile_viewers
