# Get Glassdoor company overview

Automatically get Glassdoor company overview on glassdoor.com. Company overview by employerId: name, logo, rating, review count, CEO approval, % recommend, industry/size/revenue, awards. Anonymous.

- Site: glassdoor.com
- Address: `reduck/glassdoor.com/get_company`
- Updated: 2026-08-25 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/glassdoor.com/get_company`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/glassdoor.com/get_company
```

## Input

- `employerId` (string | integer, required): Glassdoor numeric employer id (e.g. 9079 for Google), as returned by search_companies. The name slug is resolved by Glassdoor's own redirect.

## Output

- `name` (string, required)
- `employerId` (string | null, required): Numeric employer id parsed from the canonical URL
- `url` (string, optional)
- `logo` (string | null, optional)
- `size` (string | null, optional): Employee count band
- `awards` (string | null, optional)
- `rating` (number | null, optional): Overall rating out of 5
- `ceoName` (string | null, optional)
- `revenue` (string | null, optional)
- `website` (string | null, optional)
- `industry` (string | null, optional)
- `description` (string | null, optional)
- `ratingCount` (integer | null, optional)
- `ceoApprovalPct` (integer | null, optional)
- `recommendToFriendPct` (integer | null, optional)

## FAQ

### What does "Get Glassdoor company overview" do?

Company overview by employerId: name, logo, rating, review count, CEO approval, % recommend, industry/size/revenue, awards. Anonymous.

### How do I automatically get Glassdoor company overview on glassdoor.com?

Ask an AI agent connected to Reduck to run reduck/glassdoor.com/get_company, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/glassdoor.com/get_company

### Is there a glassdoor.com API to get Glassdoor company overview?

You do not need one. "Get Glassdoor company overview" drives the real glassdoor.com pages in a browser, so it works whether or not glassdoor.com offers an API for this.

### What information do I need to provide?

Required: employerId.

### What does it return?

It returns url, logo, name, size, awards, rating, ceoName, revenue, website, industry, employerId, description, ratingCount, ceoApprovalPct, recommendToFriendPct.

### Do I need to be logged in to glassdoor.com?

No. It only uses pages of glassdoor.com that are reachable without signing in.

### Does it change anything on glassdoor.com, or only read data?

It only reads. It looks things up on glassdoor.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/glassdoor.com/get_company, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/glassdoor.com/get_company

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/glassdoor.com/get_company
