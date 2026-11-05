# Update a HubSpot deal

Automatically update a HubSpot deal on app.hubspot.com. Change an existing HubSpot deal by id: its name, amount, pipeline, stage, close date, owner, deal type, priority or description. Pipeline and stage are matched by id or by the name the account shows; moving to another pipeline needs a stage of that pipeline. Fields left out are not touched, and values that already match are not sent again. The deal is read back from HubSpot afterwards and returned with the list of fields changed. Finds the account and its region automatically; pass portalId when the login has several accounts.

- Site: app.hubspot.com
- Address: `reduck/app.hubspot.com/update_deal`
- Updated: 2026-11-04 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.hubspot.com/update_deal`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.hubspot.com/update_deal
```

## Input

- `dealId` (string, required): The deal id, as list_deals or create_deal return it.
- `name` (string, optional)
- `stage` (string, optional): Stage id or name, in the deal's pipeline or the one passed.
- `amount` (number, optional)
- `ownerId` (string, optional): Owner id, as list_deals returns it in ownerId.
- `dealType` (string, optional)
- `pipeline` (string, optional): Pipeline id or name to move the deal to; pass stage with it.
- `portalId` (string, optional): The HubSpot account id, when the login has more than one.
- `priority` (string, optional)
- `closeDate` (string, optional): Expected close date, e.g. 2026-12-31.
- `description` (string, optional)

## Output

- `id` (string, required)
- `url` (string, required)
- `name` (string, required)
- `changed` (array, required): The fields this run changed.
- `owner` (string | null, optional)
- `stage` (string | null, optional)
- `amount` (number | null, optional)
- `ownerId` (string | null, optional)
- `stageId` (string | null, optional)
- `currency` (string | null, optional)
- `dealType` (string | null, optional)
- `isClosed` (boolean | null, optional)
- `pipeline` (string | null, optional)
- `priority` (string | null, optional)
- `closeDate` (string | null, optional)
- `createdAt` (string | null, optional)
- `updatedAt` (string | null, optional)
- `pipelineId` (string | null, optional)
- `description` (string | null, optional)

## FAQ

### What does "Update a HubSpot deal" do?

Change an existing HubSpot deal by id: its name, amount, pipeline, stage, close date, owner, deal type, priority or description. Pipeline and stage are matched by id or by the name the account shows; moving to another pipeline needs a stage of that pipeline. Fields left out are not touched, and values that already match are not sent again. The deal is read back from HubSpot afterwards and returned with the list of fields changed. Finds the account and its region automatically; pass portalId when the login has several accounts.

### How do I automatically update a HubSpot deal on app.hubspot.com?

Ask an AI agent connected to Reduck to run reduck/app.hubspot.com/update_deal, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.hubspot.com/update_deal

### Is there a app.hubspot.com API to update a HubSpot deal?

You do not need one. "Update a HubSpot deal" drives the real app.hubspot.com pages in a browser, so it works whether or not app.hubspot.com offers an API for this.

### What information do I need to provide?

Required: dealId. Optional: name, stage, amount, ownerId, dealType, pipeline, portalId, priority, closeDate, description.

### What does it return?

It returns id, url, name, owner, stage, amount, changed, ownerId, stageId, currency, dealType, isClosed, pipeline, priority, closeDate, createdAt, updatedAt, pipelineId, description.

### Do I need to be logged in to app.hubspot.com?

Yes. It acts as you on app.hubspot.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.hubspot.com cookies saved by the Reduck extension.

### Does it change anything on app.hubspot.com, or only read data?

It makes changes on app.hubspot.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.hubspot.com/update_deal, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.hubspot.com/update_deal

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.hubspot.com/update_deal
