# Amazon.es whoami (signed-in account)

Report which Amazon.es account this browser is signed in as: the first name shown in the header. Fails with a signed-out error when the browser is not signed in to Amazon.es.

- Site: amazon.es
- Address: `reduck/amazon.es/whoami`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.es/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.es/whoami
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `firstName` (string | null, optional)

## FAQ

### What does "Amazon.es whoami (signed-in account)" do?

Report which Amazon.es account this browser is signed in as: the first name shown in the header. Fails with a signed-out error when the browser is not signed in to Amazon.es.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, loggedIn, firstName.

### Do I need to be logged in to amazon.es?

Yes. It acts as you on amazon.es: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for amazon.es.

### Does it change anything on amazon.es, or only read data?

It only reads. It looks things up on amazon.es and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.es/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.es/whoami

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.es/whoami
