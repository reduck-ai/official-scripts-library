# Cancel a pending Sentry invitation

Automatically cancel a pending Sentry invitation on sentry.io. Cancels the pending invitation of one email in a Sentry organization. Only invitations that have not been accepted yet can be cancelled: an active member is never removed. Fails with a clear message when no pending invitation exists for that email.

- Site: sentry.io
- Address: `reduck/sentry.io/remove_pending_invite`
- Updated: 2026-11-23 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/sentry.io/remove_pending_invite`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/sentry.io/remove_pending_invite
```

## Input

- `org` (string, required): Slug of the Sentry organization, as in https://<slug>.sentry.io.
- `email` (string, required): Email address whose pending invitation must be cancelled.

## Output

- `email` (string, required)
- `cancelled` (boolean, required)

## FAQ

### What does "Cancel a pending Sentry invitation" do?

Cancels the pending invitation of one email in a Sentry organization. Only invitations that have not been accepted yet can be cancelled: an active member is never removed. Fails with a clear message when no pending invitation exists for that email.

### How do I automatically cancel a pending Sentry invitation on sentry.io?

Ask an AI agent connected to Reduck to run reduck/sentry.io/remove_pending_invite, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/sentry.io/remove_pending_invite

### Is there a sentry.io API to cancel a pending Sentry invitation?

You do not need one. "Cancel a pending Sentry invitation" drives the real sentry.io pages in a browser, so it works whether or not sentry.io offers an API for this.

### What information do I need to provide?

Required: org, email.

### What does it return?

It returns email, cancelled.

### Do I need to be logged in to sentry.io?

Yes. It acts as you on sentry.io: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the sentry.io cookies saved by the Reduck extension.

### Does it change anything on sentry.io, or only read data?

It makes changes on sentry.io, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/sentry.io/remove_pending_invite, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/sentry.io/remove_pending_invite

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/sentry.io/remove_pending_invite
