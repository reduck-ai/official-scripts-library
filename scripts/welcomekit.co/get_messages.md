# Get candidate message thread

Automatically get candidate message thread on welcomekit.co. Get the full email/message thread of one Welcome to the Jungle ATS candidate by reference, oldest first. Each message has direction (received = sent by the candidate, sent = recruiter/system), sender, plain-text body, subject, unread flag and date.

- Site: welcomekit.co
- Address: `reduck/welcomekit.co/get_messages`
- Updated: 2026-07-17 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/welcomekit.co/get_messages`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/get_messages
```

## Input

- `org` (string, required): Org reference (6-char, e.g. sfWkCZ).
- `candidateReference` (string, required): Candidate reference from list_candidates / list_notifications (format <orgprefix>-<24hex>).

## Output

- `count` (integer, required)
- `messages` (array, required)
- `candidateReference` (string, required)
- `jobReference` (string | null, optional)
- `candidateName` (string | null, optional)
- `receivedCount` (integer, optional)

## FAQ

### What does "Get candidate message thread" do?

Get the full email/message thread of one Welcome to the Jungle ATS candidate by reference, oldest first. Each message has direction (received = sent by the candidate, sent = recruiter/system), sender, plain-text body, subject, unread flag and date.

### How do I automatically get candidate message thread on welcomekit.co?

Ask an AI agent connected to Reduck to run reduck/welcomekit.co/get_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/get_messages

### Is there a welcomekit.co API to get candidate message thread?

You do not need one. "Get candidate message thread" drives the real welcomekit.co pages in a browser, so it works whether or not welcomekit.co offers an API for this.

### What information do I need to provide?

Required: org, candidateReference.

### What does it return?

It returns count, messages, jobReference, candidateName, receivedCount, candidateReference.

### Do I need to be logged in to welcomekit.co?

Yes. It acts as you on welcomekit.co: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the welcomekit.co cookies saved by the Reduck extension.

### Does it change anything on welcomekit.co, or only read data?

Unknown: its author has not declared whether it changes anything on welcomekit.co, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/welcomekit.co/get_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/get_messages

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/welcomekit.co/get_messages
