# Cancel a pending SNCF Connect train option (pre-reservation)

Automatically cancel a pending SNCF Connect train option (pre-reservation) on sncf-connect.com. Cancels a pending free option (pre-reservation) on SNCF Connect, releasing the hold it placed on a train's price and seat. Defaults to a dry run: it reports the option it would cancel and backs out without touching it. Pass confirm=true to actually cancel, which is irreversible — the blocked price is lost. When more than one option is pending, `match` picks the right one by part of its destination and/or travel date. Requires being signed in to SNCF Connect. Runs only via the local browser extension, not the hosted cloud browser.

- Site: sncf-connect.com
- Address: `reduck/sncf-connect.com/cancel_option`
- Updated: 2026-09-08 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/sncf-connect.com/cancel_option`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/sncf-connect.com/cancel_option
```

## Input

- `match` (string, optional): Substring to match against the option's title + travel date combined (e.g. 'Turin', '15 oct', 'Lyon 15 oct'); required when more than one option is pending
- `confirm` (boolean, optional): false = dry-run (report + dismiss); true = actually cancel the option

## Output

- `dryRun` (boolean, required)
- `option` (object, required)
- `cancelled` (boolean, required)
- `remainingOptions` (integer, required)
- `verified` (boolean, optional): Whether remainingOptions was confirmed against the refreshed list; false means the cancellation was accepted but the resulting count could not be verified

## FAQ

### What does "Cancel a pending SNCF Connect train option (pre-reservation)" do?

Cancels a pending free option (pre-reservation) on SNCF Connect, releasing the hold it placed on a train's price and seat. Defaults to a dry run: it reports the option it would cancel and backs out without touching it. Pass confirm=true to actually cancel, which is irreversible — the blocked price is lost. When more than one option is pending, `match` picks the right one by part of its destination and/or travel date. Requires being signed in to SNCF Connect. Runs only via the local browser extension, not the hosted cloud browser.

### How do I automatically cancel a pending SNCF Connect train option (pre-reservation) on sncf-connect.com?

Ask an AI agent connected to Reduck to run reduck/sncf-connect.com/cancel_option, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/sncf-connect.com/cancel_option

### Is there a sncf-connect.com API to cancel a pending SNCF Connect train option (pre-reservation)?

You do not need one. "Cancel a pending SNCF Connect train option (pre-reservation)" drives the real sncf-connect.com pages in a browser, so it works whether or not sncf-connect.com offers an API for this.

### What information do I need to provide?

Optional: match, confirm.

### What does it return?

It returns dryRun, option, verified, cancelled, remainingOptions.

### Do I need to be logged in to sncf-connect.com?

Yes. It acts as you on sncf-connect.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the sncf-connect.com cookies saved by the Reduck extension.

### Does it change anything on sncf-connect.com, or only read data?

It makes changes on sncf-connect.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/sncf-connect.com/cancel_option, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/sncf-connect.com/cancel_option

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/sncf-connect.com/cancel_option
