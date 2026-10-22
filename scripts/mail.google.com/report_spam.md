# Report Gmail thread as spam

Automatically report Gmail thread as spam on mail.google.com. Report a Gmail thread as spam by its hex threadId, as returned by search_emails, so it moves to the Spam folder. Returns reportedSpam and threadId only once the thread is confirmed in Spam. A thread already in Spam or in the Bin, or an id Gmail cannot open, is refused with nothing changed. Reporting also teaches Gmail's spam filter about that sender, which moving the thread back does not fully undo. Pass account when several Google accounts share the browser. For senders with an unsubscribe link Gmail asks whether to report or unsubscribe; the script never answers that question for you: it closes it and fails with nothing reported, so such mail must be reported by hand.

- Site: mail.google.com
- Address: `reduck/mail.google.com/report_spam`
- Updated: 2026-10-21 (v11)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mail.google.com/report_spam`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mail.google.com/report_spam
```

## Input

- `threadId` (string, required): Hex thread id, from the threadId field of mail.google.com/search_emails (list_inbox does not return thread ids).
- `account` (string, optional): Google account to act as: its email address, or a bare mailbox index such as "2". An address not signed in to this browser is refused with nothing reported. Omit for the first account (u/0).

## Output

- `page` (integer, required): Always 1: the thread is found with a search for its subject, not by paging All Mail. Kept for compatibility.
- `threadId` (string, required)
- `reportedSpam` (boolean, required)

## FAQ

### What does "Report Gmail thread as spam" do?

Report a Gmail thread as spam by its hex threadId, as returned by search_emails, so it moves to the Spam folder. Returns reportedSpam and threadId only once the thread is confirmed in Spam. A thread already in Spam or in the Bin, or an id Gmail cannot open, is refused with nothing changed. Reporting also teaches Gmail's spam filter about that sender, which moving the thread back does not fully undo. Pass account when several Google accounts share the browser. For senders with an unsubscribe link Gmail asks whether to report or unsubscribe; the script never answers that question for you: it closes it and fails with nothing reported, so such mail must be reported by hand.

### How do I automatically report Gmail thread as spam on mail.google.com?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/report_spam, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/report_spam

### Is there a mail.google.com API to report Gmail thread as spam?

You do not need one. "Report Gmail thread as spam" drives the real mail.google.com pages in a browser, so it works whether or not mail.google.com offers an API for this.

### What information do I need to provide?

Required: threadId. Optional: account.

### What does it return?

It returns page, threadId, reportedSpam.

### Do I need to be logged in to mail.google.com?

Yes. It acts as you on mail.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mail.google.com cookies saved by the Reduck extension.

### Does it change anything on mail.google.com, or only read data?

It makes changes on mail.google.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/report_spam, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/report_spam

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/mail.google.com/report_spam
