# Get LinkedIn profile recommendations

Automatically get LinkedIn profile recommendations on linkedin.com. Get the recommendations a LinkedIn profile has received and given, from its dedicated Recommendations page by public ID. Returns each recommendation's author/recipient (name, profile URL, connection degree, headline), the relationship note LinkedIn shows (date and how the two people worked together), and the full recommendation text. Profiles with no recommendations in a category come back with an empty list for it rather than an error. Requires being logged in to LinkedIn.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_profile_recommendations`
- Updated: 2026-09-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_profile_recommendations`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_profile_recommendations
```

## Input

- `publicId` (string, required): LinkedIn public profile id — the slug in linkedin.com/in/<publicId>/. A full profile URL is also accepted.
- `count` (integer, optional): Max entries to load per category (received/given). Omit to load all.

## Output

- `given` (array, required)
- `publicId` (string, required)
- `received` (array, required)
- `profileUrl` (string, required)

## FAQ

### What does "Get LinkedIn profile recommendations" do?

Get the recommendations a LinkedIn profile has received and given, from its dedicated Recommendations page by public ID. Returns each recommendation's author/recipient (name, profile URL, connection degree, headline), the relationship note LinkedIn shows (date and how the two people worked together), and the full recommendation text. Profiles with no recommendations in a category come back with an empty list for it rather than an error. Requires being logged in to LinkedIn.

### How do I automatically get LinkedIn profile recommendations on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_profile_recommendations, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_profile_recommendations

### Is there a linkedin.com API to get LinkedIn profile recommendations?

You do not need one. "Get LinkedIn profile recommendations" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: publicId. Optional: count.

### What does it return?

It returns given, publicId, received, profileUrl.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_profile_recommendations, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_profile_recommendations

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_profile_recommendations
