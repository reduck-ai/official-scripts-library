# Create Pipedrive lead

Automatically create Pipedrive lead on pipedrive.com. Create a new lead in Pipedrive's Leads Inbox via the "+ Lead" quick-add form, setting the contact person's name as a new contact. Returns the new lead's id and detail-page URL.

- Site: pipedrive.com
- Address: `reduck/pipedrive.com/create_lead`
- Updated: 2026-09-07 (v10)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/pipedrive.com/create_lead`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/pipedrive.com/create_lead
```

## Input

- `workspace` (string, required): Pipedrive workspace subdomain, e.g. "reduck"
- `contact_name` (string, required): Name of the contact person for this lead (created as a new contact)

## Output

- `id` (string, required)
- `url` (string, required)
- `title` (string, required)

## FAQ

### What does "Create Pipedrive lead" do?

Create a new lead in Pipedrive's Leads Inbox via the "+ Lead" quick-add form, setting the contact person's name as a new contact. Returns the new lead's id and detail-page URL.

### How do I automatically create Pipedrive lead on pipedrive.com?

Ask an AI agent connected to Reduck to run reduck/pipedrive.com/create_lead, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pipedrive.com/create_lead

### Is there a pipedrive.com API to create Pipedrive lead?

You do not need one. "Create Pipedrive lead" drives the real pipedrive.com pages in a browser, so it works whether or not pipedrive.com offers an API for this.

### What information do I need to provide?

Required: workspace, contact_name.

### What does it return?

It returns id, url, title.

### Do I need to be logged in to pipedrive.com?

Yes. It acts as you on pipedrive.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the pipedrive.com cookies saved by the Reduck extension.

### Does it change anything on pipedrive.com, or only read data?

It makes changes on pipedrive.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/pipedrive.com/create_lead, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pipedrive.com/create_lead

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/pipedrive.com/create_lead
