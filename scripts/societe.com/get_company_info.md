# Get company info

Automatically get company info on societe.com. Fetch a French company's public profile from societe.com by SIREN. Returns url, siren, name, country, status, headcount, resume, and legal.

- Site: societe.com
- Address: `reduck/societe.com/get_company_info`
- Updated: 2026-08-26 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/societe.com/get_company_info`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/societe.com/get_company_info
```

## Input

- `siren` (string, required): 9-digit SIREN

## Output

- `url` (string, required)
- `name` (string, required)
- `legal` (object, required)
- `siren` (string, required)
- `resume` (object, required)
- `status` (string | null, required)
- `country` (string | null, required)
- `headcount` (string | null, required)

## FAQ

### What does "Get company info" do?

Fetch a French company's public profile from societe.com by SIREN. Returns url, siren, name, country, status, headcount, resume, and legal.

### How do I automatically get company info on societe.com?

Ask an AI agent connected to Reduck to run reduck/societe.com/get_company_info, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/societe.com/get_company_info

### Is there a societe.com API to get company info?

You do not need one. "Get company info" drives the real societe.com pages in a browser, so it works whether or not societe.com offers an API for this.

### What information do I need to provide?

Required: siren.

### What does it return?

It returns url, name, legal, siren, resume, status, country, headcount.

### Do I need to be logged in to societe.com?

No. It only uses pages of societe.com that are reachable without signing in.

### Does it change anything on societe.com, or only read data?

It only reads. It looks things up on societe.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/societe.com/get_company_info, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/societe.com/get_company_info

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/societe.com/get_company_info
