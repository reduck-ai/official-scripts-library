# Mailchimp whoami (signed-in account)

Report which Mailchimp account this browser is signed in as: the user id, login id, email, first and last name, account name, role, plan and the account's data center (e.g. us16). Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Mailchimp scripts.

- Site: mailchimp.com
- Address: `reduck/mailchimp.com/whoami`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mailchimp.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mailchimp.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `plan` (string | null, optional)
- `role` (string | null, optional)
- `email` (string | null, optional)
- `userId` (string | null, optional)
- `loginId` (string | null, optional)
- `lastName` (string | null, optional)
- `firstName` (string | null, optional)
- `dataCenter` (string | null, optional): The account's data center (e.g. us16), which is the host prefix other Mailchimp pages use.
- `accountName` (string | null, optional)

## FAQ

### What does "Mailchimp whoami (signed-in account)" do?

Report which Mailchimp account this browser is signed in as: the user id, login id, email, first and last name, account name, role, plan and the account's data center (e.g. us16). Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Mailchimp scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns plan, role, email, userId, loginId, evidence, lastName, loggedIn, firstName, dataCenter, accountName.

### Do I need to be logged in to mailchimp.com?

Yes. It acts as you on mailchimp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mailchimp.com cookies saved by the Reduck extension.

### Does it change anything on mailchimp.com, or only read data?

It only reads. It looks things up on mailchimp.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mailchimp.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mailchimp.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/mailchimp.com/whoami
