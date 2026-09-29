# DocuSign whoami (signed-in account)

Report which DocuSign account this browser is signed in as: the user id, email, name, admin flag and permission profile, the current account's number, id and name, its regional DocuSign server, and every account the user belongs to. Being signed out is reported as a normal answer (loggedIn false), not an error. Only a sign-in that persists in the browser ("keep me signed in") is visible to runs.

- Site: docusign.com
- Address: `reduck/docusign.com/whoami`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/docusign.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/docusign.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional)
- `userId` (string | null, optional)
- `isAdmin` (boolean | null, optional)
- `accounts` (array, optional)
- `accountId` (string | null, optional): The current account's number (as shown in DocuSign settings).
- `apiBaseUri` (string | null, optional): The account's regional DocuSign server, e.g. https://eu.docusign.net.
- `accountName` (string | null, optional)
- `accountIdGuid` (string | null, optional)
- `permissionProfile` (string | null, optional)

## FAQ

### What does "DocuSign whoami (signed-in account)" do?

Report which DocuSign account this browser is signed in as: the user id, email, name, admin flag and permission profile, the current account's number, id and name, its regional DocuSign server, and every account the user belongs to. Being signed out is reported as a normal answer (loggedIn false), not an error. Only a sign-in that persists in the browser ("keep me signed in") is visible to runs.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email, userId, isAdmin, accounts, evidence, loggedIn, accountId, apiBaseUri, accountName, accountIdGuid, permissionProfile.

### Do I need to be logged in to docusign.com?

Yes. It acts as you on docusign.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the docusign.com cookies saved by the Reduck extension.

### Does it change anything on docusign.com, or only read data?

It only reads. It looks things up on docusign.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/docusign.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docusign.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/docusign.com/whoami
