# Get Partech portfolio companies

Automatically get Partech portfolio companies on partechpartners.com. Lists all companies in Partech's VC portfolio: name, status, sectors, HQ countries, funds, founders, short description and website. Reads the full portfolio in one pass rather than page by page, so the list is complete.

- Site: partechpartners.com
- Address: `reduck/partechpartners.com/get_portfolio_companies`
- Updated: 2026-08-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/partechpartners.com/get_portfolio_companies`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/partechpartners.com/get_portfolio_companies
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `companies` (array, required)

## FAQ

### What does "Get Partech portfolio companies" do?

Lists all companies in Partech's VC portfolio: name, status, sectors, HQ countries, funds, founders, short description and website. Reads the full portfolio in one pass rather than page by page, so the list is complete.

### How do I automatically get Partech portfolio companies on partechpartners.com?

Ask an AI agent connected to Reduck to run reduck/partechpartners.com/get_portfolio_companies, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/partechpartners.com/get_portfolio_companies

### Is there a partechpartners.com API to get Partech portfolio companies?

You do not need one. "Get Partech portfolio companies" drives the real partechpartners.com pages in a browser, so it works whether or not partechpartners.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, companies.

### Do I need to be logged in to partechpartners.com?

No. It only uses pages of partechpartners.com that are reachable without signing in.

### Does it change anything on partechpartners.com, or only read data?

Unknown: its author has not declared whether it changes anything on partechpartners.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/partechpartners.com/get_portfolio_companies, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/partechpartners.com/get_portfolio_companies

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/partechpartners.com/get_portfolio_companies
