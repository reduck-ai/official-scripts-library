# Adobe whoami (signed-in account)

Report which Adobe account this browser is signed in as: the Adobe ID, email, display name, first and last name, account type (personal Adobe ID vs enterprise / federated) and country. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Adobe scripts.

- Site: adobe.com
- Address: `reduck/adobe.com/whoami`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/adobe.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/adobe.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `email` (string | null, optional)
- `userId` (string | null, optional): Adobe ID (…@AdobeID).
- `lastName` (string | null, optional)
- `firstName` (string | null, optional)
- `accountType` (string | null, optional): type1 = personal Adobe ID; type2/type3 = enterprise / federated.
- `countryCode` (string | null, optional)
- `displayName` (string | null, optional)

## FAQ

### What does "Adobe whoami (signed-in account)" do?

Report which Adobe account this browser is signed in as: the Adobe ID, email, display name, first and last name, account type (personal Adobe ID vs enterprise / federated) and country. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Adobe scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns email, userId, evidence, lastName, loggedIn, firstName, accountType, countryCode, displayName.

### Do I need to be logged in to adobe.com?

Yes. It acts as you on adobe.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the adobe.com cookies saved by the Reduck extension.

### Does it change anything on adobe.com, or only read data?

It only reads. It looks things up on adobe.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/adobe.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/adobe.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/adobe.com/whoami
