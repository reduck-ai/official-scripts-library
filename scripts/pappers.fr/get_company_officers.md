# Get Pappers company officer history

Automatically get Pappers company officer history on pappers.fr. Fetches a French company's full officer history from Pappers by SIREN: both current and former officers/auditors, with role, tenure dates, and status. Complements pappers.fr/get_company, which only returns current officers — this is the affordance for "who held what role, and when" including people who've left. An unknown SIREN throws (Pappers' unknown-SIREN placeholder page lists unrelated companies' officers).

- Site: pappers.fr
- Address: `reduck/pappers.fr/get_company_officers`
- Updated: 2026-09-18 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/pappers.fr/get_company_officers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/pappers.fr/get_company_officers
```

## Input

- `siren` (string, required): SIREN (9 digits, with or without spaces)

## Output

- `siren` (string, required)
- `officers` (array, required)

## FAQ

### What does "Get Pappers company officer history" do?

Fetches a French company's full officer history from Pappers by SIREN: both current and former officers/auditors, with role, tenure dates, and status. Complements pappers.fr/get_company, which only returns current officers — this is the affordance for "who held what role, and when" including people who've left. An unknown SIREN throws (Pappers' unknown-SIREN placeholder page lists unrelated companies' officers).

### How do I automatically get Pappers company officer history on pappers.fr?

Ask an AI agent connected to Reduck to run reduck/pappers.fr/get_company_officers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pappers.fr/get_company_officers

### Is there a pappers.fr API to get Pappers company officer history?

You do not need one. "Get Pappers company officer history" drives the real pappers.fr pages in a browser, so it works whether or not pappers.fr offers an API for this.

### What information do I need to provide?

Required: siren.

### What does it return?

It returns siren, officers.

### Do I need to be logged in to pappers.fr?

No. It only uses pages of pappers.fr that are reachable without signing in.

### Does it change anything on pappers.fr, or only read data?

It only reads. It looks things up on pappers.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/pappers.fr/get_company_officers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pappers.fr/get_company_officers

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/pappers.fr/get_company_officers
