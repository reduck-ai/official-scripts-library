# Look up a French company on Infogreffe

Returns the registry record for a French company from its SIREN: registered name, trading status, registration and strike-off dates, activity, registered address, headcount, share capital and VAT number. Reads the public company page, so no account is needed.

- Site: infogreffe.fr
- Address: `reduck/infogreffe.fr/get_company`
- Updated: 2026-09-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/infogreffe.fr/get_company`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/infogreffe.fr/get_company
```

## Input

- `company` (string, required): The company's 9-digit SIREN, with or without spaces (for example 552032534 or 552 032 534), or its Infogreffe link.

## Output

- `url` (string, required)
- `name` (string | null, required)
- `siren` (string | null, required)
- `state` (string | null, required): Registry status as a code rather than the page's French wording, for example ACTIVE.
- `address` (object | null, optional): Address as declared to the register.
- `dormant` (boolean | null, optional): Whether the register records the company as having no activity.
- `activity` (object, optional)
- `headcount` (object, optional)
- `vatNumber` (string | null, optional): Intra-community VAT number. Null when the register does not carry one.
- `personType` (string | null, optional): PM for a company, PP for a sole trader.
- `soleTrader` (object | null, optional): The individual's name, when the registration is a sole trader. Null for a company.
- `legalEntity` (object | null, optional): Company-specific fields including share capital and EUID. Null for a sole trader.
- `struckOffOn` (string | null, optional): Date the company was struck off, or null while it is on the register.
- `registeredOn` (string | null, optional): Date of entry on the trade register, YYYY-MM-DD.
- `struckOffReason` (string | null, optional)

## FAQ

### What does "Look up a French company on Infogreffe" do?

Returns the registry record for a French company from its SIREN: registered name, trading status, registration and strike-off dates, activity, registered address, headcount, share capital and VAT number. Reads the public company page, so no account is needed.

### What information do I need to provide?

Required: company.

### What does it return?

It returns url, name, siren, state, address, dormant, activity, headcount, vatNumber, personType, soleTrader, legalEntity, struckOffOn, registeredOn, struckOffReason.

### Do I need to be logged in to infogreffe.fr?

No. It only uses pages of infogreffe.fr that are reachable without signing in.

### Does it change anything on infogreffe.fr, or only read data?

It only reads. It looks things up on infogreffe.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/infogreffe.fr/get_company, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/infogreffe.fr/get_company

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/infogreffe.fr/get_company
