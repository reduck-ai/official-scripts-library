# Adobe — list plans

Automatically list plans on adobe.com. List the plans on the signed-in Adobe account (Account → Plans): paid subscriptions, and free memberships (e.g. Creative Cloud Free, Document Cloud Free) with their code, name and description. Read-only; signed out is a clear error. An account with no paid plan returns an empty paid list.

- Site: adobe.com
- Address: `reduck/adobe.com/list_plans`
- Updated: 2026-09-30 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/adobe.com/list_plans`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/adobe.com/list_plans
```

## Input

It takes no input.

## Output

- `free` (array, required)
- `paid` (array, required): Paid subscriptions as Adobe's billing service returns them (offer, status, billing).
- `userId` (string | null, required)
- `paidCount` (integer, optional)

## FAQ

### What does "Adobe — list plans" do?

List the plans on the signed-in Adobe account (Account → Plans): paid subscriptions, and free memberships (e.g. Creative Cloud Free, Document Cloud Free) with their code, name and description. Read-only; signed out is a clear error. An account with no paid plan returns an empty paid list.

### How do I automatically list plans on adobe.com?

Ask an AI agent connected to Reduck to run reduck/adobe.com/list_plans, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/adobe.com/list_plans

### Is there a adobe.com API to list plans?

You do not need one. "Adobe — list plans" drives the real adobe.com pages in a browser, so it works whether or not adobe.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns free, paid, userId, paidCount.

### Do I need to be logged in to adobe.com?

Yes. It acts as you on adobe.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the adobe.com cookies saved by the Reduck extension.

### Does it change anything on adobe.com, or only read data?

It only reads. It looks things up on adobe.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/adobe.com/list_plans, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/adobe.com/list_plans

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/adobe.com/list_plans
