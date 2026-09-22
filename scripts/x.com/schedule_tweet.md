# Schedule X Post

Automatically schedule X Post on x.com. Composes a post and schedules it to send at a future date/time, instead of posting immediately.

- Site: x.com
- Address: `reduck/x.com/schedule_tweet`
- Updated: 2026-09-08 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/schedule_tweet`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/schedule_tweet
```

## Input

- `text` (string, required): The post's text. X caps this at 280 characters for a standard (non-subscriber) account.
- `sendAt` (string, required): When to send the post, as an ISO-8601 datetime (e.g. "2026-09-15T14:30:00"). X's composer only offers minute precision and reads/writes it in the account's own display timezone, not UTC — pass a naive local time (no offset) matching that timezone. X also refuses times inside the next ~10 minutes and more than ~18 months out.

## Output

- `text` (string, required)
- `send_at` (string, required)
- `scheduled_id` (string, required)

## FAQ

### What does "Schedule X Post" do?

Composes a post and schedules it to send at a future date/time, instead of posting immediately.

### How do I automatically schedule X Post on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/schedule_tweet, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/schedule_tweet

### Is there a x.com API to schedule X Post?

You do not need one. "Schedule X Post" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Required: text, sendAt.

### What does it return?

It returns text, send_at, scheduled_id.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It makes changes on x.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/schedule_tweet, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/schedule_tweet

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/schedule_tweet
