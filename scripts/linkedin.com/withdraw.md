# Withdraw LinkedIn connection invitation

Automatically withdraw LinkedIn connection invitation on linkedin.com. Withdraw a pending sent connection invitation by profile URL. Finds the "Pending" control (primary top-card action or three-dot menu item) and confirms the "Withdraw invitation?" dialog. Safe to repeat: it returns not_pending if there's no outstanding invite. After withdrawing, LinkedIn blocks resending to that person for about three weeks; it also does not unfollow them, since connecting auto-follows. Statuses: withdrawn/not_pending.

- Site: linkedin.com
- Address: `reduck/linkedin.com/withdraw`
- Updated: 2026-08-26 (v15)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/withdraw`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/withdraw
```

## Input

- `profileUrl` (string, required): LinkedIn profile URL, e.g. https://www.linkedin.com/in/emmanuelmacron/ (the /in/<publicId> form; query/locale prefixes are tolerated).

## Output

- `status` (string, required): withdrawn = the pending invitation was just withdrawn, confirmed by the pending control disappearing; not_pending = no outstanding invitation to this person.
- `publicId` (string, required): vanity id parsed from the URL (decoded)
- `profileUrl` (string, required)
- `name` (string | null, optional)
- `memberId` (string | null, optional): LinkedIn member id read from the pending control's own componentkey. Null on not_pending.

## FAQ

### What does "Withdraw LinkedIn connection invitation" do?

Withdraw a pending sent connection invitation by profile URL. Finds the "Pending" control (primary top-card action or three-dot menu item) and confirms the "Withdraw invitation?" dialog. Safe to repeat: it returns not_pending if there's no outstanding invite. After withdrawing, LinkedIn blocks resending to that person for about three weeks; it also does not unfollow them, since connecting auto-follows. Statuses: withdrawn/not_pending.

### How do I automatically withdraw LinkedIn connection invitation on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/withdraw, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/withdraw

### Is there a linkedin.com API to withdraw LinkedIn connection invitation?

You do not need one. "Withdraw LinkedIn connection invitation" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: profileUrl.

### What does it return?

It returns name, status, memberId, publicId, profileUrl.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/withdraw, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/withdraw

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/withdraw
