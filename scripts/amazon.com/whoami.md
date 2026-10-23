# Amazon whoami (signed-in account)

Report which Amazon.com account this browser is signed in as: the account's first name from the header greeting (Amazon hides the full name and email behind a password re-check). Fails with a signed-out error when the browser is not signed in to Amazon.

- Site: amazon.com
- Address: `reduck/amazon.com/whoami`
- Updated: 2026-10-22 (v10)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.com/whoami
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `firstName` (string | null, optional)

## FAQ

### What does "Amazon whoami (signed-in account)" do?

Report which Amazon.com account this browser is signed in as: the account's first name from the header greeting (Amazon hides the full name and email behind a password re-check). Fails with a signed-out error when the browser is not signed in to Amazon.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, loggedIn, firstName.

### Do I need to be logged in to amazon.com?

Yes. It acts as you on amazon.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the amazon.com cookies saved by the Reduck extension.

### Does it change anything on amazon.com, or only read data?

It only reads. It looks things up on amazon.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/amazon.com/whoami
