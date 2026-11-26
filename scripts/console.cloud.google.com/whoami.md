# Google Cloud console whoami (signed-in account)

Report which Google account the Google Cloud console is signed in as in this browser: display name and email. Fails with a sign-in error when the browser is not signed in to Google Cloud console.

- Site: console.cloud.google.com
- Address: `reduck/console.cloud.google.com/whoami`
- Updated: 2026-11-25 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/console.cloud.google.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/console.cloud.google.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional)

## FAQ

### What does "Google Cloud console whoami (signed-in account)" do?

Report which Google account the Google Cloud console is signed in as in this browser: display name and email. Fails with a sign-in error when the browser is not signed in to Google Cloud console.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email, evidence, loggedIn.

### Do I need to be logged in to console.cloud.google.com?

Yes. It acts as you on console.cloud.google.com: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for console.cloud.google.com.

### Does it change anything on console.cloud.google.com, or only read data?

It only reads. It looks things up on console.cloud.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/console.cloud.google.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/console.cloud.google.com/whoami

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/console.cloud.google.com/whoami
