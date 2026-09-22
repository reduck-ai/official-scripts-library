# Crunchbase: Get Company Profile

Automatically get Company Profile on crunchbase.com. Full company profile from Crunchbase by permalink: funding total, last round, HQ, headcount, website, contact info, socials, and operating status.

- Site: crunchbase.com
- Address: `reduck/crunchbase.com/get_company_profile`
- Updated: 2026-09-09 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/crunchbase.com/get_company_profile`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/get_company_profile
```

## Input

- `permalink` (string, required): Crunchbase permalink slug for the company, e.g. "qonto" or "pennylane" (from the crunchbase.com/organization/<permalink> URL, or from search_companies output). Case-insensitive; a full organization URL is also accepted.

## Output

- `notFound` (boolean, required): True if no company exists at this permalink on Crunchbase.
- `permalink` (string, required)
- `url` (string, optional)
- `name` (string, optional)
- `cbRank` (number | null, optional)
- `socials` (object, optional)
- `website` (string | null, optional)
- `foundedOn` (string | null, optional)
- `ipoStatus` (string | null, optional): e.g. private, public, delisted.
- `legalName` (string | null, optional)
- `categories` (array, optional)
- `phoneNumber` (string | null, optional)
- `contactEmail` (string | null, optional)
- `lastFundingAt` (string | null, optional)
- `fundingTotalUsd` (number | null, optional)
- `lastFundingType` (string | null, optional)
- `operatingStatus` (string | null, optional): e.g. active, closed.
- `numFundingRounds` (number | null, optional)
- `shortDescription` (string | null, optional)
- `numEmployeesRange` (string | null, optional)
- `headquartersLocations` (array, optional): Location hierarchy, city first.

## FAQ

### What does "Crunchbase: Get Company Profile" do?

Full company profile from Crunchbase by permalink: funding total, last round, HQ, headcount, website, contact info, socials, and operating status.

### How do I automatically get Company Profile on crunchbase.com?

Ask an AI agent connected to Reduck to run reduck/crunchbase.com/get_company_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/get_company_profile

### Is there a crunchbase.com API to get Company Profile?

You do not need one. "Crunchbase: Get Company Profile" drives the real crunchbase.com pages in a browser, so it works whether or not crunchbase.com offers an API for this.

### What information do I need to provide?

Required: permalink.

### What does it return?

It returns url, name, cbRank, socials, website, notFound, foundedOn, ipoStatus, legalName, permalink, categories, phoneNumber, contactEmail, lastFundingAt, fundingTotalUsd, lastFundingType, operatingStatus, numFundingRounds, shortDescription, numEmployeesRange, headquartersLocations.

### Do I need to be logged in to crunchbase.com?

No. It only uses pages of crunchbase.com that are reachable without signing in.

### Does it change anything on crunchbase.com, or only read data?

It only reads. It looks things up on crunchbase.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/crunchbase.com/get_company_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/get_company_profile

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/crunchbase.com/get_company_profile
