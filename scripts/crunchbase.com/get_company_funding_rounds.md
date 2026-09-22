# Crunchbase: Get Company Funding Rounds

Automatically get Company Funding Rounds on crunchbase.com. Full funding round history for one company from Crunchbase, by permalink: each round's type, date, amount raised, investor count, and lead investors.

- Site: crunchbase.com
- Address: `reduck/crunchbase.com/get_company_funding_rounds`
- Updated: 2026-07-27 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/crunchbase.com/get_company_funding_rounds`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/get_company_funding_rounds
```

## Input

- `permalink` (string, required): Crunchbase permalink slug for the company, e.g. "qonto".

## Output

- `notFound` (boolean, required)
- `permalink` (string, required)
- `fundingRounds` (array, required)

## FAQ

### What does "Crunchbase: Get Company Funding Rounds" do?

Full funding round history for one company from Crunchbase, by permalink: each round's type, date, amount raised, investor count, and lead investors.

### How do I automatically get Company Funding Rounds on crunchbase.com?

Ask an AI agent connected to Reduck to run reduck/crunchbase.com/get_company_funding_rounds, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/get_company_funding_rounds

### Is there a crunchbase.com API to get Company Funding Rounds?

You do not need one. "Crunchbase: Get Company Funding Rounds" drives the real crunchbase.com pages in a browser, so it works whether or not crunchbase.com offers an API for this.

### What information do I need to provide?

Required: permalink.

### What does it return?

It returns notFound, permalink, fundingRounds.

### Do I need to be logged in to crunchbase.com?

Yes. It acts as you on crunchbase.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the crunchbase.com cookies saved by the Reduck extension.

### Does it change anything on crunchbase.com, or only read data?

Unknown: its author has not declared whether it changes anything on crunchbase.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/crunchbase.com/get_company_funding_rounds, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/get_company_funding_rounds

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/crunchbase.com/get_company_funding_rounds
