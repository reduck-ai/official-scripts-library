# Crunchbase: Get Investor Portfolio

Automatically get Investor Portfolio on crunchbase.com. Recent portfolio investments for an investor (fund or individual) from Crunchbase, by permalink: company invested in, funding round, amount, lead-investor flag, and date. Returns the 10 most recent investments; full history requires a paid Crunchbase plan.

- Site: crunchbase.com
- Address: `reduck/crunchbase.com/get_investor_portfolio`
- Updated: 2026-07-27 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/crunchbase.com/get_investor_portfolio`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/get_investor_portfolio
```

## Input

- `permalink` (string, required): Crunchbase permalink slug for the investor (organization or person), e.g. "partech" or "edward-lando".

## Output

- `notFound` (boolean, required)
- `permalink` (string, required)
- `investments` (array, required)
- `totalNumInvestments` (number | null, required): Total funding rounds this investor has ever participated in, per its profile stat (only the most recent 10 are listed below).

## FAQ

### What does "Crunchbase: Get Investor Portfolio" do?

Recent portfolio investments for an investor (fund or individual) from Crunchbase, by permalink: company invested in, funding round, amount, lead-investor flag, and date. Returns the 10 most recent investments; full history requires a paid Crunchbase plan.

### How do I automatically get Investor Portfolio on crunchbase.com?

Ask an AI agent connected to Reduck to run reduck/crunchbase.com/get_investor_portfolio, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/get_investor_portfolio

### Is there a crunchbase.com API to get Investor Portfolio?

You do not need one. "Crunchbase: Get Investor Portfolio" drives the real crunchbase.com pages in a browser, so it works whether or not crunchbase.com offers an API for this.

### What information do I need to provide?

Required: permalink.

### What does it return?

It returns notFound, permalink, investments, totalNumInvestments.

### Do I need to be logged in to crunchbase.com?

Yes. It acts as you on crunchbase.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the crunchbase.com cookies saved by the Reduck extension.

### Does it change anything on crunchbase.com, or only read data?

Unknown: its author has not declared whether it changes anything on crunchbase.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/crunchbase.com/get_investor_portfolio, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/get_investor_portfolio

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/crunchbase.com/get_investor_portfolio
