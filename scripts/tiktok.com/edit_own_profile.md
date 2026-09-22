# Edit own TikTok profile

Automatically edit own TikTok profile on tiktok.com. Change the display name and/or bio on the TikTok account the browser is signed in as. Pass either field or both; anything you leave out is untouched. The account's own values are read first, so asking for what is already set makes no change and says so. After saving, the profile is reloaded and re-read to confirm the new values are really stored, and the handle that was edited is echoed back so you can tell which account was affected. TikTok limits display-name changes to once every seven days and will reject a second attempt inside that window. The username is deliberately not editable here: changing it also rewrites the profile link, which would break every saved link to the account.

- Site: tiktok.com
- Address: `reduck/tiktok.com/edit_own_profile`
- Updated: 2026-08-25 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/edit_own_profile`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/edit_own_profile
```

## Input

- `bio` (string, optional): New bio text. Pass an empty string to clear the bio. TikTok caps the bio at 80 characters and stores its own truncation, which is what gets reported back. Omit to leave it unchanged.
- `displayName` (string, optional): New display name (the bold name above the handle). TikTok allows this change only once every seven days and rejects it inside that window. Omit to leave it unchanged.

## Output

- `after` (object, required): Values read back from the reloaded profile after saving.
- `before` (object, required): Values read from the profile before any edit.
- `changed` (array, required): Which fields were actually written. Empty when nothing needed changing.
- `account_used` (string, required): Handle of the account that was actually edited, read from the signed-in session rather than assumed.
- `already_present` (boolean, required): True when every requested value already matched the profile, so nothing was written.
- `verified_on_page` (boolean, required): True when the profile was reloaded after saving and the stored values matched what was asked for.

## FAQ

### What does "Edit own TikTok profile" do?

Change the display name and/or bio on the TikTok account the browser is signed in as. Pass either field or both; anything you leave out is untouched. The account's own values are read first, so asking for what is already set makes no change and says so. After saving, the profile is reloaded and re-read to confirm the new values are really stored, and the handle that was edited is echoed back so you can tell which account was affected. TikTok limits display-name changes to once every seven days and will reject a second attempt inside that window. The username is deliberately not editable here: changing it also rewrites the profile link, which would break every saved link to the account.

### How do I automatically edit own TikTok profile on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/edit_own_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/edit_own_profile

### Is there a tiktok.com API to edit own TikTok profile?

You do not need one. "Edit own TikTok profile" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Optional: bio, displayName.

### What does it return?

It returns after, before, changed, account_used, already_present, verified_on_page.

### Do I need to be logged in to tiktok.com?

Yes. It acts as you on tiktok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the tiktok.com cookies saved by the Reduck extension.

### Does it change anything on tiktok.com, or only read data?

It makes changes on tiktok.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/edit_own_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/edit_own_profile

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/edit_own_profile
