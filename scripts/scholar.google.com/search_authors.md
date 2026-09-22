# Google Scholar API: search authors

Automatically search authors on scholar.google.com. Search Google Scholar's author (Profiles) directory by name/keywords. Returns each matching author's id, name, affiliation, verified-email domain, interest tags, and total cited-by count, plus a cursor for the next page.

- Site: scholar.google.com
- Address: `reduck/scholar.google.com/search_authors`
- Updated: 2026-09-18 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/scholar.google.com/search_authors`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/scholar.google.com/search_authors
```

## Input

- `query` (string, required): Author name or keywords, as typed into Google Scholar's author search.
- `cursor` (string, optional): Opaque pagination cursor from a previous call's nextCursor. Omit for the first page.

## Output

- `authors` (array, required)
- `nextCursor` (string | null, required): Pass as `cursor` to fetch the next page. null when this is the last page.

## FAQ

### What does "Google Scholar API: search authors" do?

Search Google Scholar's author (Profiles) directory by name/keywords. Returns each matching author's id, name, affiliation, verified-email domain, interest tags, and total cited-by count, plus a cursor for the next page.

### How do I automatically search authors on scholar.google.com?

Ask an AI agent connected to Reduck to run reduck/scholar.google.com/search_authors, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/scholar.google.com/search_authors

### Is there a scholar.google.com API to search authors?

You do not need one. "Google Scholar API: search authors" drives the real scholar.google.com pages in a browser, so it works whether or not scholar.google.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: cursor.

### What does it return?

It returns authors, nextCursor.

### Do I need to be logged in to scholar.google.com?

Yes. It acts as you on scholar.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the scholar.google.com cookies saved by the Reduck extension.

### Does it change anything on scholar.google.com, or only read data?

It only reads. It looks things up on scholar.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/scholar.google.com/search_authors, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/scholar.google.com/search_authors

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/scholar.google.com/search_authors
