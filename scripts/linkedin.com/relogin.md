# LinkedIn re-login

Re-establish a LinkedIn session on a browser that has signed in before, by letting LinkedIn resume a remembered session — then prove who that session belongs to by reading the member back from voyager /me, never inferring it from the argument. Optionally asserts the expected member and fails by name if the browser holds someone else's session. It never submits credentials: it takes no password, never types into the sign-in form and never reads a field's contents, so if LinkedIn asks for credentials it stops and names the human step instead.

- Site: linkedin.com
- Address: `reduck/linkedin.com/relogin`
- Updated: 2026-09-21 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/relogin`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/relogin
```

## Input

- `expectMember` (string, optional): Optional publicIdentifier (the part after /in/ in a profile URL, shaped like 'firstname-lastname-123456789') to assert the session landed as. Compared trimmed and case-insensitively. When given and the session belongs to someone else, the run fails by name rather than reporting success for the wrong account.

## Output

- `url` (string, required)
- `member` (object, required): Who the session belongs to, read back from voyager /me — never inferred from the argument.
- `method` (string, required): How the session was established. Only 'resumed' exists: LinkedIn restored a remembered session. This script never submits credentials.
- `loggedIn` (boolean, required): Always true on success — a run that cannot prove a session throws instead of returning false, so this is never a quiet negative.
- `checkedAt` (string, required)

## FAQ

### What does "LinkedIn re-login" do?

Re-establish a LinkedIn session on a browser that has signed in before, by letting LinkedIn resume a remembered session — then prove who that session belongs to by reading the member back from voyager /me, never inferring it from the argument. Optionally asserts the expected member and fails by name if the browser holds someone else's session. It never submits credentials: it takes no password, never types into the sign-in form and never reads a field's contents, so if LinkedIn asks for credentials it stops and names the human step instead.

### What information do I need to provide?

Optional: expectMember.

### What does it return?

It returns url, member, method, loggedIn, checkedAt.

### Do I need to be logged in to linkedin.com?

No. It only uses pages of linkedin.com that are reachable without signing in.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/relogin, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/relogin

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/relogin
