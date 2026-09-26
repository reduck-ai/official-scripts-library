# Create or update a HubSpot contact

Automatically create or update a HubSpot contact on app.hubspot.com. Create a HubSpot contact from an email address, or update the existing one's first and last name when that email is already on the account — never a duplicate. Reports created, updated or unchanged (nothing saved when the values already match), and re-reads the contact afterwards to confirm. On accounts with GDPR features on, creating needs legalBasis (the caller chooses it; it is never defaulted). dry_run fills everything in and stops before saving. Finds the right account and regional host automatically.

- Site: app.hubspot.com
- Address: `reduck/app.hubspot.com/create_or_update_contact`
- Updated: 2026-09-25 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.hubspot.com/create_or_update_contact`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.hubspot.com/create_or_update_contact
```

## Input

- `email` (string, required): The contact's email address. This is the key: an address already on the account is updated rather than duplicated.
- `dry_run` (boolean, optional): When true, works out whether the contact exists and fills the form, then stops before saving. Nothing is created or changed.
- `lastName` (string, optional)
- `portalId` (string, optional): The HubSpot account id, when the login has more than one. Omit it to use the default account.
- `firstName` (string, optional)
- `legalBasis` (string, optional): GDPR legal basis for processing the contact's data, used when creating. Required on accounts with GDPR features on (HubSpot will not create the contact without it); ignored for an existing contact. Never defaulted — the caller must choose it.

## Output

- `email` (string, required)
- `saved` (boolean, required): True only when a save happened AND the contact was re-read with the requested values.
- `action` (string, required): created / updated = saved and confirmed; unchanged = the contact exists and already has these values, so nothing was saved; would_* = dry run.
- `dryRun` (boolean, required)
- `portalId` (string, required)
- `changed` (array, optional): Which fields were changed on an existing contact.
- `contactId` (string | null, optional)
- `contactUrl` (string | null, optional)
- `accountUsed` (string | null, optional)
- `existedBefore` (boolean, optional)

## FAQ

### What does "Create or update a HubSpot contact" do?

Create a HubSpot contact from an email address, or update the existing one's first and last name when that email is already on the account — never a duplicate. Reports created, updated or unchanged (nothing saved when the values already match), and re-reads the contact afterwards to confirm. On accounts with GDPR features on, creating needs legalBasis (the caller chooses it; it is never defaulted). dry_run fills everything in and stops before saving. Finds the right account and regional host automatically.

### How do I automatically create or update a HubSpot contact on app.hubspot.com?

Ask an AI agent connected to Reduck to run reduck/app.hubspot.com/create_or_update_contact, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.hubspot.com/create_or_update_contact

### Is there a app.hubspot.com API to create or update a HubSpot contact?

You do not need one. "Create or update a HubSpot contact" drives the real app.hubspot.com pages in a browser, so it works whether or not app.hubspot.com offers an API for this.

### What information do I need to provide?

Required: email. Optional: dry_run, lastName, portalId, firstName, legalBasis.

### What does it return?

It returns email, saved, action, dryRun, changed, portalId, contactId, contactUrl, accountUsed, existedBefore.

### Do I need to be logged in to app.hubspot.com?

Yes. It acts as you on app.hubspot.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.hubspot.com cookies saved by the Reduck extension.

### Does it change anything on app.hubspot.com, or only read data?

It makes changes on app.hubspot.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.hubspot.com/create_or_update_contact, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.hubspot.com/create_or_update_contact

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.hubspot.com/create_or_update_contact
