# Station F HAL whoami (signed-in account)

Report which Station F HAL account this browser is signed in as: the account email. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other HAL scripts.

- Site: hal.stationf.co
- Address: `reduck/hal.stationf.co/whoami`
- Updated: 2026-09-30 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hal.stationf.co/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hal.stationf.co/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `email` (string | null, optional)

## FAQ

### What does "Station F HAL whoami (signed-in account)" do?

Report which Station F HAL account this browser is signed in as: the account email. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other HAL scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns email, evidence, loggedIn.

### Do I need to be logged in to hal.stationf.co?

Yes. It acts as you on hal.stationf.co: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the hal.stationf.co cookies saved by the Reduck extension.

### Does it change anything on hal.stationf.co, or only read data?

It only reads. It looks things up on hal.stationf.co and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hal.stationf.co/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hal.stationf.co/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/hal.stationf.co/whoami
