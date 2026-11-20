# Facebook whoami (signed-in account)

Report which Facebook account this browser is signed in as: the user id and name, and whether it acts as a Page. A browser held at a Facebook security checkpoint is reported as such. A signed-out browser fails with a signed-out error asking you to sign in to Facebook, so it can be used to check a session before running other Facebook scripts. It never signs in.

- Site: facebook.com
- Address: `reduck/facebook.com/whoami`
- Updated: 2026-11-19 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/facebook.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/facebook.com/whoami
```

## Input

It takes no input.

## Output

- `id` (string | null, required): Kept for older callers; same as userId.
- `name` (string | null, required)
- `state` (string, required)
- `actingId` (string | null, required)
- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `actingAsPage` (boolean, required)
- `userId` (string | null, optional): User id of the signed-in account (whoami format).

## FAQ

### What does "Facebook whoami (signed-in account)" do?

Report which Facebook account this browser is signed in as: the user id and name, and whether it acts as a Page. A browser held at a Facebook security checkpoint is reported as such. A signed-out browser fails with a signed-out error asking you to sign in to Facebook, so it can be used to check a session before running other Facebook scripts. It never signs in.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns id, name, state, userId, actingId, evidence, loggedIn, actingAsPage.

### Do I need to be logged in to facebook.com?

Yes. It acts as you on facebook.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the facebook.com cookies saved by the Reduck extension.

### Does it change anything on facebook.com, or only read data?

It only reads. It looks things up on facebook.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/facebook.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/facebook.com/whoami
