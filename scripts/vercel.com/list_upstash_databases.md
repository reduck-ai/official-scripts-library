# List Upstash Redis databases of a Vercel team and their access

Automatically list Upstash Redis databases of a Vercel team and their access on vercel.com. Lists the Upstash databases attached to a Vercel team through the Upstash integration, opens each one in the Upstash console through Vercel's single sign-on, and returns its name, plan, region and access control users as the console shows them. Secrets and tokens are never returned. Read-only. Fails with a sign-in error when the browser is not signed in to Vercel.

- Site: vercel.com
- Address: `reduck/vercel.com/list_upstash_databases`
- Updated: 2026-11-17 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/vercel.com/list_upstash_databases`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/vercel.com/list_upstash_databases
```

## Input

- `team` (string, required): Vercel team slug, for example conception-ai.

## Output

- `team` (string, required)
- `count` (number, required)
- `databases` (array, required)

## FAQ

### What does "List Upstash Redis databases of a Vercel team and their access" do?

Lists the Upstash databases attached to a Vercel team through the Upstash integration, opens each one in the Upstash console through Vercel's single sign-on, and returns its name, plan, region and access control users as the console shows them. Secrets and tokens are never returned. Read-only. Fails with a sign-in error when the browser is not signed in to Vercel.

### How do I automatically list Upstash Redis databases of a Vercel team and their access on vercel.com?

Ask an AI agent connected to Reduck to run reduck/vercel.com/list_upstash_databases, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/vercel.com/list_upstash_databases

### Is there a vercel.com API to list Upstash Redis databases of a Vercel team and their access?

You do not need one. "List Upstash Redis databases of a Vercel team and their access" drives the real vercel.com pages in a browser, so it works whether or not vercel.com offers an API for this.

### What information do I need to provide?

Required: team.

### What does it return?

It returns team, count, databases.

### Do I need to be logged in to vercel.com?

Yes. It acts as you on vercel.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the vercel.com cookies saved by the Reduck extension.

### Does it change anything on vercel.com, or only read data?

It only reads. It looks things up on vercel.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/vercel.com/list_upstash_databases, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/vercel.com/list_upstash_databases

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/vercel.com/list_upstash_databases
