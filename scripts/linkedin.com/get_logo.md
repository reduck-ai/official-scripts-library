# Get LinkedIn company/showcase logo

Automatically get LinkedIn company/showcase logo on linkedin.com. Get the logo image URL from a LinkedIn company page (/company/<slug>) or showcase page (/showcase/<slug>), by URL or bare slug (bare slug assumes company). Works for both company and showcase pages. Returns null logoUrl on pages with no logo set.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_logo`
- Updated: 2026-09-03 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_logo`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_logo
```

## Input

- `url` (string, required): LinkedIn company URL (e.g. https://www.linkedin.com/company/goldman-sachs), showcase URL (e.g. https://www.linkedin.com/showcase/skills-problem-solving/), or bare company slug (e.g. goldman-sachs).

## Output

- `name` (string, required)
- `logoUrl` (string | null, required): Highest-resolution logo artifact URL, or null if the page has no logo set.
- `finalUrl` (string, required): URL after LinkedIn's redirect (renamed slugs, canonical tab).
- `pageType` (string, required): COMPANY or SHOWCASE.
- `logoFilename` (string | null, required): Suggested filename for the downloaded logo (<universalName>-logo.<ext>), or null if logoUrl is null.
- `requestedUrl` (string, required)
- `logoLocalPath` (string | null, required): Local filesystem path where the logo image was downloaded (session-scoped temp location), or null if logoUrl is null.
- `universalName` (string, required)

## FAQ

### What does "Get LinkedIn company/showcase logo" do?

Get the logo image URL from a LinkedIn company page (/company/<slug>) or showcase page (/showcase/<slug>), by URL or bare slug (bare slug assumes company). Works for both company and showcase pages. Returns null logoUrl on pages with no logo set.

### How do I automatically get LinkedIn company/showcase logo on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_logo, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_logo

### Is there a linkedin.com API to get LinkedIn company/showcase logo?

You do not need one. "Get LinkedIn company/showcase logo" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns name, logoUrl, finalUrl, pageType, logoFilename, requestedUrl, logoLocalPath, universalName.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_logo, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_logo

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_logo
