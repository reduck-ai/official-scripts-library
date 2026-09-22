# Get Google Scholar author's papers

Automatically get Google Scholar author's papers on scholar.google.com. Fetch a Google Scholar author's profile (name, affiliation, verified-email domain, interest tags, citation metrics) plus their publication list, sorted by citation count as the profile itself shows. Google Scholar loads 20 papers at a time behind a "Show more" click; pass count to load further pages (capped at what the profile actually has).

- Site: scholar.google.com
- Address: `reduck/scholar.google.com/get_author_papers`
- Updated: 2026-09-13 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/scholar.google.com/get_author_papers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/scholar.google.com/get_author_papers
```

## Input

- `authorId` (string, required): Scholar author id (the user= param), as returned by search_authors.
- `count` (integer, optional): How many papers to return, at most. Google Scholar loads them 20 at a time behind its own "Show more" button; pass a higher count to click through more pages. Defaults to the first page (20).

## Output

- `author` (object, required)
- `papers` (array, required)

## FAQ

### What does "Get Google Scholar author's papers" do?

Fetch a Google Scholar author's profile (name, affiliation, verified-email domain, interest tags, citation metrics) plus their publication list, sorted by citation count as the profile itself shows. Google Scholar loads 20 papers at a time behind a "Show more" click; pass count to load further pages (capped at what the profile actually has).

### How do I automatically get Google Scholar author's papers on scholar.google.com?

Ask an AI agent connected to Reduck to run reduck/scholar.google.com/get_author_papers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/scholar.google.com/get_author_papers

### Is there a scholar.google.com API to get Google Scholar author's papers?

You do not need one. "Get Google Scholar author's papers" drives the real scholar.google.com pages in a browser, so it works whether or not scholar.google.com offers an API for this.

### What information do I need to provide?

Required: authorId. Optional: count.

### What does it return?

It returns author, papers.

### Do I need to be logged in to scholar.google.com?

No. It only uses pages of scholar.google.com that are reachable without signing in.

### Does it change anything on scholar.google.com, or only read data?

It only reads. It looks things up on scholar.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/scholar.google.com/get_author_papers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/scholar.google.com/get_author_papers

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/scholar.google.com/get_author_papers
