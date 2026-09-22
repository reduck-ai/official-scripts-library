# Telegram — Get the signed-in account's profile

Automatically get the signed-in account's profile on web.telegram.org. Read the profile of the Telegram account this browser is signed in as: its display name, the phone number on the account, and the presence label shown beneath the name. Useful for confirming which account a run will act as before doing anything that writes. Does not include username, bio or birthday — Telegram keeps those behind its Edit profile form rather than on the settings screen.

- Site: web.telegram.org
- Address: `reduck/web.telegram.org/get_own_profile`
- Updated: 2026-09-17 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.telegram.org/get_own_profile`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/get_own_profile
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required): Whether this browser has a usable Telegram session. False is a normal result, not a failure, so this can be polled on a schedule without the check counting against its own health.
- `phone` (string | null, optional): The phone number on the account, as Telegram formats it for display (e.g. "+33 6 79 34 83 25"). Null if the settings screen showed no phone row, or when there is no session.
- `evidence` (string | null, optional): Only set when loggedIn is false: what proved the session absent, so a genuine signed-out reading can be told from a broken run.
- `displayName` (string | null, optional): The account's display name — first and last name combined, as shown under the avatar. Null when there is no session.
- `statusLabel` (string | null, optional): The presence line beneath the name, verbatim. This one IS translated ("online", "last seen recently", …), so treat it as a display string and do not branch on its text.

## FAQ

### What does "Telegram — Get the signed-in account's profile" do?

Read the profile of the Telegram account this browser is signed in as: its display name, the phone number on the account, and the presence label shown beneath the name. Useful for confirming which account a run will act as before doing anything that writes. Does not include username, bio or birthday — Telegram keeps those behind its Edit profile form rather than on the settings screen.

### How do I automatically get the signed-in account's profile on web.telegram.org?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/get_own_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/get_own_profile

### Is there a web.telegram.org API to get the signed-in account's profile?

You do not need one. "Telegram — Get the signed-in account's profile" drives the real web.telegram.org pages in a browser, so it works whether or not web.telegram.org offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns phone, evidence, loggedIn, displayName, statusLabel.

### Do I need to be logged in to web.telegram.org?

No. It only uses pages of web.telegram.org that are reachable without signing in.

### Does it change anything on web.telegram.org, or only read data?

It only reads. It looks things up on web.telegram.org and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/get_own_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/get_own_profile

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.telegram.org/get_own_profile
