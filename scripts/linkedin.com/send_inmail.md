# Send a LinkedIn InMail

Automatically send a LinkedIn InMail on linkedin.com. Send a paid InMail to an out-of-network LinkedIn profile via the profile's InMail CTA (consumes an InMail credit). Distinct from send_message, which only reaches 1st-degree and open profiles. dryRun (default true) opens the composer and reports what it found without sending.

- Site: linkedin.com
- Address: `reduck/linkedin.com/send_inmail`
- Updated: 2026-08-26 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/send_inmail`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/send_inmail
```

## Input

- `text` (string, required): InMail body.
- `subject` (string, required): InMail subject line. Ignored when the composer that opens is the free-message one, which has no subject field.
- `profileUrl` (string, required): LinkedIn profile URL or public id of the recipient.
- `dryRun` (boolean, optional): Defaults to true, and fills the composer and resolves the real Send control without clicking it. Must be explicitly false to spend an InMail credit and deliver a real message. A dry run may leave an unsent draft in the composer.

## Output

- `status` (string, required): "dry_run" means Send was resolved but never clicked. "no_inmail_cta" means this seat has no InMail route to the member.
- `subject` (string, required)
- `recipient` (string | null, required)
- `profileUrl` (string, required)
- `diagnostics` (object, optional): How the route and the Send control were resolved. Any button text here is diagnostics only, never a selector.
- `creditsBefore` (number | null, optional): InMail credits read off the composer, or null when the composer showed no credit line. Never inferred.
- `creditsRemainingAfter` (number | null, optional): Always null after a send: once the composer closes the credit line is gone, and a loose match reads unrelated numbers.

## FAQ

### What does "Send a LinkedIn InMail" do?

Send a paid InMail to an out-of-network LinkedIn profile via the profile's InMail CTA (consumes an InMail credit). Distinct from send_message, which only reaches 1st-degree and open profiles. dryRun (default true) opens the composer and reports what it found without sending.

### How do I automatically send a LinkedIn InMail on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/send_inmail, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/send_inmail

### Is there a linkedin.com API to send a LinkedIn InMail?

You do not need one. "Send a LinkedIn InMail" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: profileUrl, subject, text. Optional: dryRun.

### What does it return?

It returns status, subject, recipient, profileUrl, diagnostics, creditsBefore, creditsRemainingAfter.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/send_inmail, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/send_inmail

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/send_inmail
