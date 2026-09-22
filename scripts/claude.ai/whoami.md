# Who am I on Claude.ai

Report which Claude.ai account the browser is signed in as: id (the sign-in email, the identifier a connector for this host is labelled with), full name and display name (the name in the sidebar's bottom-left corner), the account uuid, plus every organisation it belongs to with the role held there and the subscription plan (free, pro, max, team, enterprise). Throws when signed out. Use it before any other claude.ai script to confirm the session, or to pick the organisation uuid another script needs.

- Site: claude.ai
- Address: `reduck/claude.ai/whoami`
- Updated: 2026-09-17 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/claude.ai/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/claude.ai/whoami
```

## Input

It takes no input.

## Output

- `id` (string, required): The account's sign-in email; the identifier a connector for claude.ai is labelled with.
- `orgs` (array, required): Every organisation the account is a member of. A personal account has exactly one.
- `uuid` (string, required): The account's uuid.
- `full_name` (string, required): The name given at signup.
- `display_name` (string, required): The name Claude greets the user with and shows in the sidebar; equal to full_name unless changed in settings.

## FAQ

### What does "Who am I on Claude.ai" do?

Report which Claude.ai account the browser is signed in as: id (the sign-in email, the identifier a connector for this host is labelled with), full name and display name (the name in the sidebar's bottom-left corner), the account uuid, plus every organisation it belongs to with the role held there and the subscription plan (free, pro, max, team, enterprise). Throws when signed out. Use it before any other claude.ai script to confirm the session, or to pick the organisation uuid another script needs.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns id, orgs, uuid, full_name, display_name.

### Do I need to be logged in to claude.ai?

Yes. It acts as you on claude.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the claude.ai cookies saved by the Reduck extension.

### Does it change anything on claude.ai, or only read data?

It only reads. It looks things up on claude.ai and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/claude.ai/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/claude.ai/whoami
