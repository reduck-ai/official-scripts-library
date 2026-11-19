# Uber Eats whoami (signed-in account)

Report which Uber Eats account this browser is signed in as: the account name, the email when Uber Eats exposes it, and a hashed email that identifies the account otherwise. When the browser is signed out of Uber Eats, the run fails with a signed-out error asking you to sign in to ubereats.com.

- Site: ubereats.com
- Address: `reduck/ubereats.com/whoami`
- Updated: 2026-11-18 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ubereats.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ubereats.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional)
- `userId` (string | null, optional): Uber user uuid.
- `account` (string | null, optional): What the account signs in with: the email when exposed, else the phone number.
- `hashedEmail` (string | null, optional)

## FAQ

### What does "Uber Eats whoami (signed-in account)" do?

Report which Uber Eats account this browser is signed in as: the account name, the email when Uber Eats exposes it, and a hashed email that identifies the account otherwise. When the browser is signed out of Uber Eats, the run fails with a signed-out error asking you to sign in to ubereats.com.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email, userId, account, evidence, loggedIn, hashedEmail.

### Do I need to be logged in to ubereats.com?

Yes. It acts as you on ubereats.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the ubereats.com cookies saved by the Reduck extension.

### Does it change anything on ubereats.com, or only read data?

It only reads. It looks things up on ubereats.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ubereats.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ubereats.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/ubereats.com/whoami
