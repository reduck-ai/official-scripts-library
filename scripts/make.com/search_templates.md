# Search Make.com public templates

Automatically search Make.com public templates on make.com. Search Make's public template catalogue by name and/or by the apps a template uses.

- Site: make.com
- Address: `reduck/make.com/search_templates`
- Updated: 2026-09-09 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/make.com/search_templates`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/make.com/search_templates
```

## Input

- `name` (string, optional): Free-text match on the template name, as typed into the "Search by apps or name" box (the "Search for <text>" option). Omit for the unfiltered catalogue.
- `usedApps` (array, optional): App slugs a template must use, as picked from the search box's app chips — e.g. ["slack","google-sheets"]. These are exactly the values returned in each record's usedApps, so results feed back in as filters. Combined with `name` if both are given.

## Output

- `count` (integer, required): Templates actually returned in this response.
- `templates` (array, required)
- `totalCount` (integer, required): Total matches the catalogue holds for this filter, which is larger than `count` — the grid loads only its first page and Make exposes no caller-addressable offset (pg[*] in the page URL is ignored).

## FAQ

### What does "Search Make.com public templates" do?

Search Make's public template catalogue by name and/or by the apps a template uses.

### How do I automatically search Make.com public templates on make.com?

Ask an AI agent connected to Reduck to run reduck/make.com/search_templates, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/make.com/search_templates

### Is there a make.com API to search Make.com public templates?

You do not need one. "Search Make.com public templates" drives the real make.com pages in a browser, so it works whether or not make.com offers an API for this.

### What information do I need to provide?

Optional: name, usedApps.

### What does it return?

It returns count, templates, totalCount.

### Do I need to be logged in to make.com?

Yes. It acts as you on make.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the make.com cookies saved by the Reduck extension.

### Does it change anything on make.com, or only read data?

It only reads. It looks things up on make.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/make.com/search_templates, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/make.com/search_templates

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/make.com/search_templates
