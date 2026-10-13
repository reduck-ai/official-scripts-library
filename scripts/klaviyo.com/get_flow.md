# Get Klaviyo flow

Automatically get Klaviyo flow on klaviyo.com. Read one Klaviyo flow by its flowId from list_flows: name, status, trigger, filters and every step in order (emails, SMS, delays) with each message's name, subject and sender. Fails with a clear error when the flow does not exist.

- Site: klaviyo.com
- Address: `reduck/klaviyo.com/get_flow`
- Updated: 2026-10-12 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/klaviyo.com/get_flow`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/klaviyo.com/get_flow
```

## Input

- `flowId` (string, required): Flow id from list_flows, e.g. WdxTFf.

## Output

- `name` (string, required)
- `steps` (array, required)
- `flowId` (string, required)
- `url` (string, optional)
- `status` (string, optional)
- `created` (string | null, optional)
- `reentry` (object | null, optional)
- `trigger` (object, optional)
- `updated` (string | null, optional)
- `archived` (boolean, optional)
- `timezone` (string | null, optional)
- `startPathId` (string | null, optional)
- `profileFilter` (string | null, optional)

## FAQ

### What does "Get Klaviyo flow" do?

Read one Klaviyo flow by its flowId from list_flows: name, status, trigger, filters and every step in order (emails, SMS, delays) with each message's name, subject and sender. Fails with a clear error when the flow does not exist.

### How do I automatically get Klaviyo flow on klaviyo.com?

Ask an AI agent connected to Reduck to run reduck/klaviyo.com/get_flow, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/klaviyo.com/get_flow

### Is there a klaviyo.com API to get Klaviyo flow?

You do not need one. "Get Klaviyo flow" drives the real klaviyo.com pages in a browser, so it works whether or not klaviyo.com offers an API for this.

### What information do I need to provide?

Required: flowId.

### What does it return?

It returns url, name, steps, flowId, status, created, reentry, trigger, updated, archived, timezone, startPathId, profileFilter.

### Do I need to be logged in to klaviyo.com?

Yes. It acts as you on klaviyo.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the klaviyo.com cookies saved by the Reduck extension.

### Does it change anything on klaviyo.com, or only read data?

It only reads. It looks things up on klaviyo.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/klaviyo.com/get_flow, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/klaviyo.com/get_flow

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/klaviyo.com/get_flow
