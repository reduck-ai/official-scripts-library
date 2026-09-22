# Remove team member (Claude.ai)

Automatically remove team member (Claude.ai) on claude.ai. Remove a member from a Claude.ai Team or organisation by email, with built-in verification. Records the member list before and after and returns removed / verified / collateralLoss, giving you proof the right person was removed and nobody else was affected. The removal is guarded: it proceeds only once the confirmation step names the target email. dryRun (default true) walks up to the confirmation and cancels without removing — set it false to remove for real. Requires being signed in to claude.ai as an organisation owner or admin. Works with the interface in French or English, and reads the current members page, so it suits teams that fit on one page.

- Site: claude.ai
- Address: `reduck/claude.ai/delete_user`
- Updated: 2026-09-15 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/claude.ai/delete_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/claude.ai/delete_user
```

## Input

- `email` (string, required): Email of the team member to remove
- `dryRun` (boolean, optional): If true (default), walks to the confirmation dialog then cancels without removing. Set false to actually remove.

## Output

- `email` (string, required)
- `found` (boolean, required)
- `dryRun` (boolean, required)
- `removed` (boolean, required)
- `gate` (string | null, optional)
- `after` (object, optional)
- `before` (object, optional)
- `verified` (boolean, optional)
- `collateralLoss` (array, optional)

## FAQ

### What does "Remove team member (Claude.ai)" do?

Remove a member from a Claude.ai Team or organisation by email, with built-in verification. Records the member list before and after and returns removed / verified / collateralLoss, giving you proof the right person was removed and nobody else was affected. The removal is guarded: it proceeds only once the confirmation step names the target email. dryRun (default true) walks up to the confirmation and cancels without removing — set it false to remove for real. Requires being signed in to claude.ai as an organisation owner or admin. Works with the interface in French or English, and reads the current members page, so it suits teams that fit on one page.

### How do I automatically remove team member (Claude.ai) on claude.ai?

Ask an AI agent connected to Reduck to run reduck/claude.ai/delete_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/delete_user

### Is there a claude.ai API to remove team member (Claude.ai)?

You do not need one. "Remove team member (Claude.ai)" drives the real claude.ai pages in a browser, so it works whether or not claude.ai offers an API for this.

### What information do I need to provide?

Required: email. Optional: dryRun.

### What does it return?

It returns gate, after, email, found, before, dryRun, removed, verified, collateralLoss.

### Do I need to be logged in to claude.ai?

Yes. It acts as you on claude.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the claude.ai cookies saved by the Reduck extension.

### Does it change anything on claude.ai, or only read data?

It makes changes on claude.ai, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/claude.ai/delete_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/delete_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/claude.ai/delete_user
