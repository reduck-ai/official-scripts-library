# Find LinkedIn newsletters by author

Automatically find LinkedIn newsletters by author on linkedin.com. List the LinkedIn newsletters published by a given profile or company page. For a profile, reads its Featured section (the dedicated Featured details page); for a company page, reads its Newsletter module on the page's Home tab. Returns each newsletter's name, URL, cadence/subscriber line, description, and logo. An author with no newsletter featured or listed there comes back with an empty list rather than an error.

- Site: linkedin.com
- Address: `reduck/linkedin.com/find_newsletters_by_author`
- Updated: 2026-09-08 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/find_newsletters_by_author`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/find_newsletters_by_author
```

## Input

- `authorUrl` (string, required): A LinkedIn profile URL (https://www.linkedin.com/in/<publicId>/) or company page URL (https://www.linkedin.com/company/<slug>/).

## Output

- `authorType` (string, required): person | company, resolved from the input URL's path.
- `newsletters` (array, required): Empty when the author has no newsletter featured (profile) or listed (company).

## FAQ

### What does "Find LinkedIn newsletters by author" do?

List the LinkedIn newsletters published by a given profile or company page. For a profile, reads its Featured section (the dedicated Featured details page); for a company page, reads its Newsletter module on the page's Home tab. Returns each newsletter's name, URL, cadence/subscriber line, description, and logo. An author with no newsletter featured or listed there comes back with an empty list rather than an error.

### How do I automatically find LinkedIn newsletters by author on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/find_newsletters_by_author, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/find_newsletters_by_author

### Is there a linkedin.com API to find LinkedIn newsletters by author?

You do not need one. "Find LinkedIn newsletters by author" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: authorUrl.

### What does it return?

It returns authorType, newsletters.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/find_newsletters_by_author, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/find_newsletters_by_author

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/find_newsletters_by_author
