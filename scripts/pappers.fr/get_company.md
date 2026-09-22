# Pappers company profile

Fetches a company's Pappers profile from its SIREN. Returns name, siren, address, postal_code, city, head_office_siret, naf_code, naf_label, legal_form, share_capital, creation_date, workforce, status, business_sector and officers (display_name, role, since, to, former, age, is_legal_entity, siren, first_name, last_name) — both current and past officers, people and legal entities alike; a legal-entity officer carries its own 9-digit siren and no age. An unknown SIREN throws rather than returning data: Pappers answers it with a placeholder page whose officer block lists unrelated companies. Phone, website and email are not included since they are reserved for Pappers accounts; use google.com/search_places instead.

- Site: pappers.fr
- Address: `reduck/pappers.fr/get_company`
- Updated: 2026-09-14 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/pappers.fr/get_company`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/pappers.fr/get_company
```

## Input

- `siren` (string, required): SIREN (9 digits, with or without spaces)

## Output

- `url` (string, optional)
- `city` (string | null, optional)
- `name` (string | null, optional): Legal name, without Pappers' trade-name aliases.
- `siren` (string, optional)
- `status` (string | null, optional): "active" or "inactive"
- `address` (string | null, optional)
- `naf_code` (string | null, optional)
- `officers` (array, optional): Both current and former officers, with mandate dates.
- `naf_label` (string | null, optional)
- `workforce` (string | null, optional)
- `legal_form` (string | null, optional)
- `postal_code` (string | null, optional)
- `creation_date` (string | null, optional)
- `share_capital` (string | null, optional)
- `business_sector` (string | null, optional)
- `head_office_siret` (string | null, optional)

## FAQ

### What does "Pappers company profile" do?

Fetches a company's Pappers profile from its SIREN. Returns name, siren, address, postal_code, city, head_office_siret, naf_code, naf_label, legal_form, share_capital, creation_date, workforce, status, business_sector and officers (display_name, role, since, to, former, age, is_legal_entity, siren, first_name, last_name) — both current and past officers, people and legal entities alike; a legal-entity officer carries its own 9-digit siren and no age. An unknown SIREN throws rather than returning data: Pappers answers it with a placeholder page whose officer block lists unrelated companies. Phone, website and email are not included since they are reserved for Pappers accounts; use google.com/search_places instead.

### What information do I need to provide?

Required: siren.

### What does it return?

It returns url, city, name, siren, status, address, naf_code, officers, naf_label, workforce, legal_form, postal_code, creation_date, share_capital, business_sector, head_office_siret.

### Do I need to be logged in to pappers.fr?

No. It only uses pages of pappers.fr that are reachable without signing in.

### Does it change anything on pappers.fr, or only read data?

It only reads. It looks things up on pappers.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/pappers.fr/get_company, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pappers.fr/get_company

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/pappers.fr/get_company
