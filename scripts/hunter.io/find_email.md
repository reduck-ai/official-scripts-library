# Find Email (Hunter)

Automatically find Email (Hunter) on hunter.io. Looks up a person's professional email address at a company domain, via Hunter's public Email Finder tool.

- Site: hunter.io
- Address: `reduck/hunter.io/find_email`
- Updated: 2026-09-03 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hunter.io/find_email`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hunter.io/find_email
```

## Input

- `domain` (string, required): The company's domain, e.g. "microsoft.com" (no protocol, no www).
- `fullName` (string, required): The person's full name, e.g. "Satya Nadella".

## Output

- `email` (string | null, required)
- `found` (boolean, required)
- `domain` (string, required)
- `company` (string | null, required)
- `full_name` (string, required)
- `linkedin_url` (string | null, required)
- `confidence_score` (integer | null, required)

## FAQ

### What does "Find Email (Hunter)" do?

Looks up a person's professional email address at a company domain, via Hunter's public Email Finder tool.

### How do I automatically find Email (Hunter) on hunter.io?

Ask an AI agent connected to Reduck to run reduck/hunter.io/find_email, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hunter.io/find_email

### Is there a hunter.io API to find Email (Hunter)?

You do not need one. "Find Email (Hunter)" drives the real hunter.io pages in a browser, so it works whether or not hunter.io offers an API for this.

### What information do I need to provide?

Required: fullName, domain.

### What does it return?

It returns email, found, domain, company, full_name, linkedin_url, confidence_score.

### Do I need to be logged in to hunter.io?

No. It only uses pages of hunter.io that are reachable without signing in.

### Does it change anything on hunter.io, or only read data?

It only reads. It looks things up on hunter.io and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hunter.io/find_email, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hunter.io/find_email

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/hunter.io/find_email
