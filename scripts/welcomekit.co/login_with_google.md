# Welcome to the Jungle login (Google SSO)

Sign in to the Welcome to the Jungle recruiting dashboard (welcomekit.co) with a Google account already signed in on this browser, so the other welcomekit.co scripts can run straight afterwards. The Google account must have a seat on the Welcome to the Jungle organisation. Pass the account email to pick which Google account to use; without it the first account in Google's chooser is taken, which may not be the one with a seat. Optionally pass the organisation reference to open. Returns whether the session was already open or newly created, and the dashboard it landed on. If Google asks to approve Welcome to the Jungle's access to the account, the run stops there unless you pass approveConsent as true. Only do that together with the email of the account you mean to approve, once you have decided to grant that access. It also stops, and says why, when Google asks for a security check, when the account is not available in the browser, or when the account has no seat on the organisation. Needs your own browser where the account is already signed in to Google, so it cannot run on a shared cloud browser.

- Site: welcomekit.co
- Address: `reduck/welcomekit.co/login_with_google`
- Updated: 2026-10-06 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/welcomekit.co/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/login_with_google
```

## Input

- `org` (string, optional): ATS organization reference (the segment after /dashboard/o/ in the dashboard URL). Optional. If omitted, the script opens the signed-in account's default dashboard instead of a specific organisation.
- `email` (string, optional): Google account email to sign in with (must have an active Google session in this browser). Optional. If omitted, the script signs in with the FIRST Google account listed in the account chooser, so pass it whenever the browser has several Google accounts to avoid signing in with the wrong one.
- `approveConsent` (boolean, optional): Set true ONLY if you have already decided to grant Welcome to the Jungle's Google sign-in access to this account. Default false: the run stops at Google's consent screen instead of approving it.

## Output

- `url` (string, required)
- `method` (string, required)
- `authenticated` (boolean, required)
- `org` (string | null, optional)
- `email` (string | null, optional)

## FAQ

### What does "Welcome to the Jungle login (Google SSO)" do?

Sign in to the Welcome to the Jungle recruiting dashboard (welcomekit.co) with a Google account already signed in on this browser, so the other welcomekit.co scripts can run straight afterwards. The Google account must have a seat on the Welcome to the Jungle organisation. Pass the account email to pick which Google account to use; without it the first account in Google's chooser is taken, which may not be the one with a seat. Optionally pass the organisation reference to open. Returns whether the session was already open or newly created, and the dashboard it landed on. If Google asks to approve Welcome to the Jungle's access to the account, the run stops there unless you pass approveConsent as true. Only do that together with the email of the account you mean to approve, once you have decided to grant that access. It also stops, and says why, when Google asks for a security check, when the account is not available in the browser, or when the account has no seat on the organisation. Needs your own browser where the account is already signed in to Google, so it cannot run on a shared cloud browser.

### What information do I need to provide?

Optional: org, email, approveConsent.

### What does it return?

It returns org, url, email, method, authenticated.

### Do I need to be logged in to welcomekit.co?

No. It only uses pages of welcomekit.co that are reachable without signing in.

### Does it change anything on welcomekit.co, or only read data?

It makes changes on welcomekit.co, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/welcomekit.co/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/welcomekit.co/login_with_google
