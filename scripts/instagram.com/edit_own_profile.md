# Edit Instagram bio

Automatically edit Instagram bio on instagram.com. Update the signed-in Instagram account's bio ("Presentación"/About text shown on the profile). Running it again with the same text does nothing new — it reports no change instead of resubmitting. Website and username/name fields aren't editable from this page (Instagram restricts them to the mobile app / Meta Accounts Center), so only bio is covered.

- Site: instagram.com
- Address: `reduck/instagram.com/edit_own_profile`
- Updated: 2026-09-03 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/edit_own_profile`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/edit_own_profile
```

## Input

- `bio` (string, required): New bio text (max 150 characters, matching Instagram's own limit). Pass an empty string to clear the bio.

## Output

- `bio` (string, required): The bio now set on the account.
- `changed` (boolean, required): false when the requested bio already matched the current one and no submit was needed.

## FAQ

### What does "Edit Instagram bio" do?

Update the signed-in Instagram account's bio ("Presentación"/About text shown on the profile). Running it again with the same text does nothing new — it reports no change instead of resubmitting. Website and username/name fields aren't editable from this page (Instagram restricts them to the mobile app / Meta Accounts Center), so only bio is covered.

### How do I automatically edit Instagram bio on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/edit_own_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/edit_own_profile

### Is there a instagram.com API to edit Instagram bio?

You do not need one. "Edit Instagram bio" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: bio.

### What does it return?

It returns bio, changed.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It makes changes on instagram.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/edit_own_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/edit_own_profile

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/edit_own_profile
