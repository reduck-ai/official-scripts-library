# Search Gmail

Automatically search Gmail on mail.google.com. Takes any Gmail search query and returns up to 50 matching threads as JSON, each with a reusable threadId.

- Site: mail.google.com
- Address: `reduck/mail.google.com/search_emails`
- Updated: 2026-10-05 (v9)
- Author: Reduck AI (reduck)

## About

Any operator the Gmail search box understands works here, because the query runs in your own signed-in Gmail, and each match comes back with a threadId the other Gmail scripts accept. Say a bookkeeper closing September runs has:attachment filename:pdf subject:(invoice OR receipt) after:2026/09/01 before:2026/10/01 with limit set to 50. She gets 34 threads, comfortably under the cap, hands each threadId to download_attachment and drops the PDFs into the accounting tool, binning the inline logos that come along. Each result is a thread, and only the first results page is read: 20 rows by default, 50 at most. On personal accounts Gmail's default sort for search is Most relevant, so those rows are the top of a ranking, not necessarily the newest matches. The date field is Gmail's tooltip text in your account language, so parse it before sorting. On a long back-and-forth, sender is whoever is listed first on the row, often not the last person to reply.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mail.google.com/search_emails`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mail.google.com/search_emails
```

## Input

- `query` (string, required): Gmail search query; full native operator syntax (from:, subject:, has:attachment, after:...).
- `limit` (integer, optional): Max rows to return (1-50, default 20).
- `account` (string, optional): Gmail account address to act as (authuser pin). Omit for u/0.

## Output

- `n` (integer, required)
- `query` (string, required)
- `emails` (array, required)

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "n": 3,
  "query": "…",
  "emails": [
    {}
  ]
}
```

## FAQ

### What does "Search Gmail" do?

Search the signed-in Gmail with the native query syntax (from:, to:, subject:, has:attachment, after:/before:, labels…) and return matching threads: threadId (feed it to get_thread / reply_to_email), sender, senderEmail, subject, snippet, date, unread, starred, hasAttachment. Results are threads rather than individual messages, which is Gmail's own search granularity, and only the first page of results is returned (up to 50).

### How do I automatically search Gmail on mail.google.com?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/search_emails, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/search_emails

### Is there a mail.google.com API to search Gmail?

You do not need one. "Search Gmail" drives the real mail.google.com pages in a browser, so it works whether or not mail.google.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: limit, account.

### What does it return?

It returns n, query, emails.

### Do I need to be logged in to mail.google.com?

Yes. It acts as you on mail.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mail.google.com cookies saved by the Reduck extension.

### Does it change anything on mail.google.com, or only read data?

It only reads. It looks things up on mail.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/search_emails, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/search_emails

### Who maintains it?

It is part of Reduck's official curated catalogue.

### Can it return more than 50 Gmail results, or the second page?

Search Gmail reads only the first page of results: 20 threads unless you pass a higher limit, 50 at most, and fewer if your Gmail Maximum page size setting is under 50. The output carries no total match count, so when n equals your limit there may be more; split the query into date windows with after: and before: and narrow each window until n comes back below the limit.

### Will the results match what the Gmail API returns for the same query?

Google's filtering guide says the Gmail API's q parameter skips two things the search box does: thread-wide search, and alias expansion, where a search on your main Workspace address also catches mail sent from your aliases. Search Gmail uses the search box itself, so it gets both. The API is free for standard use and can page through a whole mailbox at up to 500 threads per call, but every scope that allows a query is restricted, so an app offered to the public must pass Google's verification, while personal use under 100 users, testing mode and apps internal to a Workspace organization are exempt.

### Why doesn't it find an email sitting in Spam or Trash?

Gmail leaves Spam and Trash out of a standard search, and Search Gmail runs that same search, so a plain query skips them. Add in:anywhere to the query when you are hunting for a confirmation or password reset email that may have been filtered.

### Can I archive, label or trash the threads it finds?

The threadId from Search Gmail feeds archive_email, add_label, trash_email and mark_read. trash_email and mark_read only look through the first four All Mail list pages (about 200 threads at 50 per page, fewer with a smaller page size), so an old match can be out of their reach, while archive_email falls back to opening the thread by its id when it is not among the newest Inbox pages.

Source: https://reduck.ai/explore/scripts/reduck/mail.google.com/search_emails
