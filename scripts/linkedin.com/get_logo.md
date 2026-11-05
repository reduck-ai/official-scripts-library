# Get LinkedIn company/showcase logo

Automatically get LinkedIn company/showcase logo on linkedin.com. Download the logo of a LinkedIn company or showcase page, by URL or bare slug (bare slug means company). Returns the logo image URL, the saved file's path and its filename; logoUrl is null when the page has no logo.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_logo`
- Updated: 2026-11-04 (v10)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_logo`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_logo
```

## Input

- `url` (string, required): LinkedIn company URL (e.g. https://www.linkedin.com/company/goldman-sachs), showcase URL (e.g. https://www.linkedin.com/showcase/skills-problem-solving/), or bare company slug (e.g. goldman-sachs).

## Output

- `url` (string | null, required): Link to the saved logo when the browser is a cloud browser; null on your own Chrome or when there is no logo.
- `name` (string, required)
- `path` (string | null, required): Where the logo was saved on the machine running your Chrome; null on a cloud browser or when there is no logo.
- `logoUrl` (string | null, required): Highest-resolution logo artifact URL, or null if the page has no logo set.
- `finalUrl` (string, required): URL after LinkedIn's redirect (renamed slugs, canonical tab).
- `pageType` (string, required): COMPANY or SHOWCASE.
- `logoFilename` (string | null, required): Suggested filename for the downloaded logo (<universalName>-logo.<ext>), or null if logoUrl is null.
- `requestedUrl` (string, required)
- `logoLocalPath` (string | null, required): Same as path, or url on a cloud browser; kept for existing callers. Null if logoUrl is null.
- `universalName` (string, required)

## FAQ

### What does "Get LinkedIn company/showcase logo" do?

Download the logo of a LinkedIn company or showcase page, by URL or bare slug (bare slug means company). Returns the logo image URL, the saved file's path and its filename; logoUrl is null when the page has no logo.

### How do I automatically get LinkedIn company/showcase logo on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_logo, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_logo

### Is there a linkedin.com API to get LinkedIn company/showcase logo?

You do not need one. "Get LinkedIn company/showcase logo" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns url, name, path, logoUrl, finalUrl, pageType, logoFilename, requestedUrl, logoLocalPath, universalName.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_logo, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_logo

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_logo
