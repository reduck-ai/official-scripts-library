# Welcome Kit — list job candidates (SSO)

Automatically list job candidates (SSO) on welcometothejungle.com. List all candidates of a Welcome Kit (WTTJ) job by org + job reference, via Welcome to the Jungle SSO: name, headline, pipeline stage name, resume URL, cover letter and contacts.

- Site: welcometothejungle.com
- Address: `reduck/welcometothejungle.com/list_welcomekit_candidates`
- Updated: 2026-09-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/welcometothejungle.com/list_welcomekit_candidates`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/welcometothejungle.com/list_welcomekit_candidates
```

## Input

- `jobReference` (string, required): Job reference from the job URL, e.g. 'REDUC_4w6OLNW'.
- `organizationReference` (string, required): Org slug from the dashboard URL, e.g. 'sfWkCZ'.
- `perPage` (number, optional): Max candidates to fetch (default 100).

## FAQ

### What does "Welcome Kit — list job candidates (SSO)" do?

List all candidates of a Welcome Kit (WTTJ) job by org + job reference, via Welcome to the Jungle SSO: name, headline, pipeline stage name, resume URL, cover letter and contacts.

### How do I automatically list job candidates (SSO) on welcometothejungle.com?

Ask an AI agent connected to Reduck to run reduck/welcometothejungle.com/list_welcomekit_candidates, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcometothejungle.com/list_welcomekit_candidates

### Is there a welcometothejungle.com API to list job candidates (SSO)?

You do not need one. "Welcome Kit — list job candidates (SSO)" drives the real welcometothejungle.com pages in a browser, so it works whether or not welcometothejungle.com offers an API for this.

### What information do I need to provide?

Required: organizationReference, jobReference. Optional: perPage.

### Do I need to be logged in to welcometothejungle.com?

Yes. It acts as you on welcometothejungle.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the welcometothejungle.com cookies saved by the Reduck extension.

### Does it change anything on welcometothejungle.com, or only read data?

Unknown: its author has not declared whether it changes anything on welcometothejungle.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/welcometothejungle.com/list_welcomekit_candidates, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcometothejungle.com/list_welcomekit_candidates

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/welcometothejungle.com/list_welcomekit_candidates
