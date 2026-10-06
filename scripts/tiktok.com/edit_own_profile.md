# Edit own TikTok profile

Automatically edit own TikTok profile on tiktok.com. Sets a new display name, bio or both, then reloads the profile to report what TikTok actually stored.

- Site: tiktok.com
- Address: `reduck/tiktok.com/edit_own_profile`
- Updated: 2026-10-05 (v2)
- Author: Reduck AI (reduck)

## About

Rewriting a TikTok bio from an agent pays off when the bio changes on a schedule. Take a streamer's assistant who has Claude rewrite it every Monday with that week's live slot, say "Live Thu 8pm CET". Back come the old and new text plus account_used, the handle that got the edit. When the slot has not moved, nothing is written and already_present comes back true, so the weekly job can fire without checking first. For a one-off promo, save before.bio. That string is what you send afterwards to put the usual bio back. Interface language does not matter, since the form is found by TikTok's data-e2e markers, not button labels. If the cookie banner is up, the run clicks its first button (decline optional cookies), because the banner covers Save. TikTok's Display API reads display_name and bio_description through GET /v2/user/info/ but has no write endpoint, hence the trip through the profile editor in a signed-in browser.

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

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "after": {
    "bio": "…",
    "displayName": "…"
  },
  "before": {
    "bio": "…",
    "displayName": "…"
  },
  "changed": [
    "displayName"
  ],
  "account_used": "…",
  "already_present": true,
  "verified_on_page": true
}
```

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

It makes changes on tiktok.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/edit_own_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/edit_own_profile

### Who maintains it?

It is part of Reduck's official curated catalogue.

### Can it change my TikTok username or profile photo?

Only the display name and the bio get written, and the @username and profile photo are left alone. The username is also your tiktok.com/@ address and links to the old address stop working after a change, so do that one yourself in TikTok's edit profile screen once you are ready to update every link-in-bio page that points to it.

### What happens if I changed my TikTok display name less than seven days ago?

TikTok allows one display name change every seven days, and a run that asks for a new displayName inside that window ends in an error instead of returning before and after values. If a bio went in the same run, check it with the get_profile script before retrying, then send the bio on its own until the week is up.

### Why does my TikTok profile still show the old bio after the change?

TikTok serves a cached copy of the profile page for a short while after a save, and a profile tab that was already open does not redraw its header. The run reloads the profile up to six times and only reports success once the new text is in the page data, so if after.bio shows your new bio, the change is stored and a later refresh will show it.

### Which TikTok account does it edit if I manage several?

The edit lands on whichever TikTok account is signed in on the browser it runs in, and that handle comes back as account_used; no input picks a different account. Before touching a client's profile, run the TikTok whoami script to check the session, and if it shows the wrong account, sign that browser in to the client's account first (log out and back in, or use a separate browser profile).

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/edit_own_profile
