# Facebook whoami (signed-in account)

Report which Facebook account this browser is signed in as: the user id and name. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Facebook scripts. It never signs in.

- Site: facebook.com
- Address: `reduck/facebook.com/whoami`
- Updated: 2026-11-13 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/facebook.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/facebook.com/whoami
```

## Input

It takes no input.

## Output

- `id` (string | null, required): User id of the signed-in account; null when signed out.
- `name` (string | null, required): Display name of the identity the browser acts as.
- `state` (string, required): ok: signed in. logged_out: no account signed in. checkpoint: Facebook holds the session at a security check the user must pass in the browser.
- `actingId` (string | null, required): Id of the identity the browser acts as: the account itself, or the Page it is switched to.
- `evidence` (string, required)
- `loggedIn` (boolean, required): True when a Facebook account is signed in and usable (state ok).
- `actingAsPage` (boolean, required): True when the account is switched to a Page: posts, comments and group membership are then the Page's, not the personal profile's.

## FAQ

### What does "Facebook whoami (signed-in account)" do?

Report which Facebook account this browser is signed in as: the user id and name. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Facebook scripts. It never signs in.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns id, name, state, actingId, evidence, loggedIn, actingAsPage.

### Do I need to be logged in to facebook.com?

Yes. It acts as you on facebook.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the facebook.com cookies saved by the Reduck extension.

### Does it change anything on facebook.com, or only read data?

It only reads. It looks things up on facebook.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/facebook.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/facebook.com/whoami
