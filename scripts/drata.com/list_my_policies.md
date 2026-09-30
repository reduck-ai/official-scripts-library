# Drata: list my policies

Automatically list my policies on drata.com. List the Drata policies assigned to the signed-in employee, with each policy's name, description, published date and whether (and when) the employee accepted it, plus totals. Read-only; it never accepts a policy.

- Site: drata.com
- Address: `reduck/drata.com/list_my_policies`
- Updated: 2026-09-29 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/drata.com/list_my_policies`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/drata.com/list_my_policies
```

## Input

It takes no input.

## Output

- `total` (integer, required)
- `accepted` (integer, required)
- `policies` (array, required)
- `workspaceSlug` (string | null, optional)

## FAQ

### What does "Drata: list my policies" do?

List the Drata policies assigned to the signed-in employee, with each policy's name, description, published date and whether (and when) the employee accepted it, plus totals. Read-only; it never accepts a policy.

### How do I automatically list my policies on drata.com?

Ask an AI agent connected to Reduck to run reduck/drata.com/list_my_policies, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drata.com/list_my_policies

### Is there a drata.com API to list my policies?

You do not need one. "Drata: list my policies" drives the real drata.com pages in a browser, so it works whether or not drata.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns total, accepted, policies, workspaceSlug.

### Do I need to be logged in to drata.com?

Yes. It acts as you on drata.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the drata.com cookies saved by the Reduck extension.

### Does it change anything on drata.com, or only read data?

It only reads. It looks things up on drata.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/drata.com/list_my_policies, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drata.com/list_my_policies

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/drata.com/list_my_policies
