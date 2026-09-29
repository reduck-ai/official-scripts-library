# Hugging Face whoami (signed-in account)

Report which Hugging Face account this browser is signed in as: the user id, Hub username, full name, email (and whether it is verified), Pro status, and every organization with the account's role there. Being signed out — including a stale session cookie — is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Hugging Face scripts.

- Site: huggingface.co
- Address: `reduck/huggingface.co/whoami`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/huggingface.co/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/huggingface.co/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `orgs` (array, optional)
- `email` (string | null, optional)
- `isPro` (boolean | null, optional)
- `userId` (string | null, optional)
- `fullName` (string | null, optional)
- `username` (string | null, optional): The Hub handle (huggingface.co/<username>).
- `emailVerified` (boolean | null, optional)

## FAQ

### What does "Hugging Face whoami (signed-in account)" do?

Report which Hugging Face account this browser is signed in as: the user id, Hub username, full name, email (and whether it is verified), Pro status, and every organization with the account's role there. Being signed out — including a stale session cookie — is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Hugging Face scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns orgs, email, isPro, userId, evidence, fullName, loggedIn, username, emailVerified.

### Do I need to be logged in to huggingface.co?

Yes. It acts as you on huggingface.co: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the huggingface.co cookies saved by the Reduck extension.

### Does it change anything on huggingface.co, or only read data?

It only reads. It looks things up on huggingface.co and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/huggingface.co/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/huggingface.co/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/huggingface.co/whoami
