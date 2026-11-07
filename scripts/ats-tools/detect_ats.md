# Detect the Greenhouse, Lever or Ashby board behind a company careers page

Automatically detect the Greenhouse, Lever or Ashby board behind a company careers page on ats-tools. Given a company's own careers page URL, tells whether its job board runs on Greenhouse, Lever or Ashby and returns the board slug, and whether the page's network traffic or its links revealed it. Returns platform, slug and signal as null when the page shows no such sign, which is common for companies that host their board on their own site; that is an answer, not a failure.

- Site: ats-tools
- Address: `reduck/ats-tools/detect_ats`
- Updated: 2026-11-06 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ats-tools/detect_ats`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ats-tools/detect_ats
```

## Input

- `url` (string, required): URL of the company's careers/jobs page, e.g. https://discord.com/careers

## Output

- `url` (string, required)
- `slug` (string | null, required)
- `signal` (string | null, required)
- `platform` (string | null, required)

## FAQ

### What does "Detect the Greenhouse, Lever or Ashby board behind a company careers page" do?

Given a company's own careers page URL, tells whether its job board runs on Greenhouse, Lever or Ashby and returns the board slug, and whether the page's network traffic or its links revealed it. Returns platform, slug and signal as null when the page shows no such sign, which is common for companies that host their board on their own site; that is an answer, not a failure.

### How do I automatically detect the Greenhouse, Lever or Ashby board behind a company careers page on ats-tools?

Ask an AI agent connected to Reduck to run reduck/ats-tools/detect_ats, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ats-tools/detect_ats

### Is there a ats-tools API to detect the Greenhouse, Lever or Ashby board behind a company careers page?

You do not need one. "Detect the Greenhouse, Lever or Ashby board behind a company careers page" drives the real ats-tools pages in a browser, so it works whether or not ats-tools offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns url, slug, signal, platform.

### Do I need to be logged in to ats-tools?

No. It only uses pages of ats-tools that are reachable without signing in.

### Does it change anything on ats-tools, or only read data?

Unknown: its author has not declared whether it changes anything on ats-tools, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ats-tools/detect_ats, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ats-tools/detect_ats

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/ats-tools/detect_ats
