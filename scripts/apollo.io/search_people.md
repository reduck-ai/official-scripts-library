# Search Apollo people by job title

Automatically search Apollo people by job title on apollo.io. Search Apollo's people database by job title (Find People, Job Titles filter). Returns name, title, company, location, LinkedIn URL, and email status for each match on the requested page.

- Site: apollo.io
- Address: `reduck/apollo.io/search_people`
- Updated: 2026-09-11 (v13)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/apollo.io/search_people`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/apollo.io/search_people
```

## Input

- `job_title` (string, required): Job title to search for, e.g. "CEO" or "marketing manager". Apollo's title field accepts free text: it offers whatever you type back as a selectable suggestion, so a title nobody holds - or a typo - is searched rather than refused, and comes back as totalEntries 0 with an empty people list. Treat 0 results as "Apollo found nobody for this exact string", which a misspelling also produces; it is not proof the role does not exist. The script does still refuse to commit a title other than the one asked for.

## Output

- `people` (array, required)
- `job_title` (string, required)
- `totalEntries` (integer | null, required)

## FAQ

### What does "Search Apollo people by job title" do?

Search Apollo's people database by job title (Find People, Job Titles filter). Returns name, title, company, location, LinkedIn URL, and email status for each match on the requested page.

### How do I automatically search Apollo people by job title on apollo.io?

Ask an AI agent connected to Reduck to run reduck/apollo.io/search_people, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/apollo.io/search_people

### Is there a apollo.io API to search Apollo people by job title?

You do not need one. "Search Apollo people by job title" drives the real apollo.io pages in a browser, so it works whether or not apollo.io offers an API for this.

### What information do I need to provide?

Required: job_title.

### What does it return?

It returns people, job_title, totalEntries.

### Do I need to be logged in to apollo.io?

Yes. It acts as you on apollo.io: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the apollo.io cookies saved by the Reduck extension.

### Does it change anything on apollo.io, or only read data?

It only reads. It looks things up on apollo.io and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/apollo.io/search_people, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/apollo.io/search_people

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/apollo.io/search_people
