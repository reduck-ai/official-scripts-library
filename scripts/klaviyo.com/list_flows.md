# List Klaviyo flows

Automatically list Klaviyo flows on klaviyo.com. List the email and SMS flows in the signed-in Klaviyo account with their flowId, status, trigger, channels and last-30-day stats. Paged; pass archived to list archived flows. An account with no flows returns an empty list.

- Site: klaviyo.com
- Address: `reduck/klaviyo.com/list_flows`
- Updated: 2026-10-22 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/klaviyo.com/list_flows`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/klaviyo.com/list_flows
```

## Input

- `page` (integer, optional): Page number, starting at 1.
- `archived` (boolean, optional): true lists archived flows instead of active ones.
- `pageSize` (integer, optional): Flows per page.

## Output

- `flows` (array, required)
- `total` (integer, required)
- `page` (integer, optional)
- `hasMore` (boolean, optional)
- `pageSize` (integer, optional)

## FAQ

### What does "List Klaviyo flows" do?

List the email and SMS flows in the signed-in Klaviyo account with their flowId, status, trigger, channels and last-30-day stats. Paged; pass archived to list archived flows. An account with no flows returns an empty list.

### How do I automatically list Klaviyo flows on klaviyo.com?

Ask an AI agent connected to Reduck to run reduck/klaviyo.com/list_flows, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/klaviyo.com/list_flows

### Is there a klaviyo.com API to list Klaviyo flows?

You do not need one. "List Klaviyo flows" drives the real klaviyo.com pages in a browser, so it works whether or not klaviyo.com offers an API for this.

### What information do I need to provide?

Optional: page, archived, pageSize.

### What does it return?

It returns page, flows, total, hasMore, pageSize.

### Do I need to be logged in to klaviyo.com?

Yes. It acts as you on klaviyo.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the klaviyo.com cookies saved by the Reduck extension.

### Does it change anything on klaviyo.com, or only read data?

It only reads. It looks things up on klaviyo.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/klaviyo.com/list_flows, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/klaviyo.com/list_flows

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/klaviyo.com/list_flows
