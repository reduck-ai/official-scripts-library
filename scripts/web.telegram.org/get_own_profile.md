# Telegram — Get the signed-in account's profile

Automatically get the signed-in account's profile on web.telegram.org. Read the profile of the Telegram account this browser is signed in as: its display name, the phone number on the account, and the presence label shown beneath the name. Useful for confirming which account a run will act as before doing anything that writes. When this browser is not signed in to Telegram Web, the run fails with a signed-out error that says to sign in there. Does not include username, bio or birthday: Telegram keeps those behind its Edit profile form rather than on the settings screen.

- Site: web.telegram.org
- Address: `reduck/web.telegram.org/get_own_profile`
- Updated: 2026-10-20 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.telegram.org/get_own_profile`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/get_own_profile
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required): Always true: a run that returns has read a signed-in Telegram session.
- `phone` (string | null, optional): The phone number on the account, as Telegram formats it for display (e.g. "+33 6 12 34 56 78"). Null if the settings screen showed no phone row.
- `evidence` (string | null, optional): Always null: a signed-out browser now fails the run with a signed-out error instead of returning a result.
- `displayName` (string | null, optional): The account's display name: first and last name combined, as shown under the avatar.
- `statusLabel` (string | null, optional): The presence line beneath the name, verbatim. It is translated ("online", "last seen recently", …), so treat it as a display string and do not branch on its text.

## FAQ

### What does "Telegram — Get the signed-in account's profile" do?

Read the profile of the Telegram account this browser is signed in as: its display name, the phone number on the account, and the presence label shown beneath the name. Useful for confirming which account a run will act as before doing anything that writes. When this browser is not signed in to Telegram Web, the run fails with a signed-out error that says to sign in there. Does not include username, bio or birthday: Telegram keeps those behind its Edit profile form rather than on the settings screen.

### How do I automatically get the signed-in account's profile on web.telegram.org?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/get_own_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/get_own_profile

### Is there a web.telegram.org API to get the signed-in account's profile?

You do not need one. "Telegram — Get the signed-in account's profile" drives the real web.telegram.org pages in a browser, so it works whether or not web.telegram.org offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns phone, evidence, loggedIn, displayName, statusLabel.

### Do I need to be logged in to web.telegram.org?

Yes. It acts as you on web.telegram.org: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.telegram.org cookies saved by the Reduck extension.

### Does it change anything on web.telegram.org, or only read data?

It only reads. It looks things up on web.telegram.org and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/get_own_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/get_own_profile

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.telegram.org/get_own_profile
