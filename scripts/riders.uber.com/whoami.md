# Uber whoami (signed-in rider account)

Report which Uber rider account this browser is signed in as: the rider id, first and last name, email and phone number. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Uber rider scripts.

- Site: riders.uber.com
- Address: `reduck/riders.uber.com/whoami`
- Updated: 2026-09-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/riders.uber.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/riders.uber.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `email` (string | null, optional)
- `phone` (string | null, optional): Phone number as Uber formats it, e.g. "+33 6 12 34 56 78".
- `userId` (string | null, optional): The rider's Uber uuid.
- `lastName` (string | null, optional)
- `firstName` (string | null, optional)

## FAQ

### What does "Uber whoami (signed-in rider account)" do?

Report which Uber rider account this browser is signed in as: the rider id, first and last name, email and phone number. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Uber rider scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns email, phone, userId, evidence, lastName, loggedIn, firstName.

### Do I need to be logged in to riders.uber.com?

Yes. It acts as you on riders.uber.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the riders.uber.com cookies saved by the Reduck extension.

### Does it change anything on riders.uber.com, or only read data?

It only reads. It looks things up on riders.uber.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/riders.uber.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/riders.uber.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/riders.uber.com/whoami
