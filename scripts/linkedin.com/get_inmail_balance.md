# Get LinkedIn InMail credit balance

Automatically get LinkedIn InMail credit balance on linkedin.com. Read the account's remaining InMail credits from the LinkedIn Premium / Sales Navigator subscription page. Returns creditsRemaining plus creditsTotal and a reset date where LinkedIn shows them, and says which surface the figure came from.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_inmail_balance`
- Updated: 2026-09-03 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_inmail_balance`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_inmail_balance
```

## Input

- `profileUrl` (string, required): A LinkedIn profile URL or public id of any out-of-network 2nd/3rd-degree member this account can InMail. Used only to open the compose panel that displays the balance -- no message is sent. Any valid InMail-eligible target works; the returned balance is an account-level figure, not specific to this person.

## Output

- `canInmail` (boolean, required): True when this account has an InMail route to profileUrl and the composer showed a real 'Use N of M credits' line.
- `profileUrl` (string, required)
- `creditsRemaining` (integer | null, required): Live remaining InMail credit balance, read from the compose panel's 'Use 1 of N credits' line. Null when no InMail route exists to profileUrl, or the composer that opened was a free-message one (member already reachable, no credit involved).
- `note` (string | null, optional): Explains why canInmail is false or creditsRemaining is null, when applicable.

## FAQ

### What does "Get LinkedIn InMail credit balance" do?

Read the account's remaining InMail credits from the LinkedIn Premium / Sales Navigator subscription page. Returns creditsRemaining plus creditsTotal and a reset date where LinkedIn shows them, and says which surface the figure came from.

### How do I automatically get LinkedIn InMail credit balance on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_inmail_balance, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_inmail_balance

### Is there a linkedin.com API to get LinkedIn InMail credit balance?

You do not need one. "Get LinkedIn InMail credit balance" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: profileUrl.

### What does it return?

It returns note, canInmail, profileUrl, creditsRemaining.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_inmail_balance, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_inmail_balance

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_inmail_balance
