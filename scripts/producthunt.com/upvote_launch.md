# Upvote a Product Hunt launch

Automatically upvote a Product Hunt launch on producthunt.com. Upvote a launch on Product Hunt as the signed-in account. Product Hunt's vote control is a toggle, so this script checks whether the account has already upvoted the launch and leaves it alone if so, rather than pressing the control and silently removing an existing vote. The result reports the account that voted, whether the vote was already there, the launch's score afterwards, and confirmation read back from Product Hunt's own response rather than from the button. Accepts a full launch URL or a "product/launch" slug pair. Pair it with the remove-upvote script to undo. Note that Product Hunt votes on a launch, not on a product as a whole: a product with several launches is upvoted one launch at a time.

- Site: producthunt.com
- Address: `reduck/producthunt.com/upvote_launch`
- Updated: 2026-08-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/producthunt.com/upvote_launch`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/producthunt.com/upvote_launch
```

## Input

- `launch` (string, required): Full launch URL (e.g. "https://www.producthunt.com/products/notion/launches/notion-mail") or a "product/launch" slug pair (e.g. "notion/notion-mail").

## Output

- `hasVoted` (boolean, required): Whether the account holds an upvote on this launch after the run. True on success.
- `launchUrl` (string, required)
- `account_used` (string, required): Handle of the account that voted, read from the signed-in session rather than assumed.
- `already_present` (boolean, required): True when this account had already upvoted the launch, so nothing was pressed.
- `verified_on_page` (boolean, required): True when Product Hunt's own response for the vote confirmed the launch is now upvoted.
- `postId` (string | null, optional): Product Hunt's numeric id for the launch that was voted on.
- `scoreAfter` (number | null, optional): Score Product Hunt reported with the vote. Other people vote continuously, so this is their number at that instant, not necessarily scoreBefore + 1.
- `scoreBefore` (number | null, optional): Score shown on the control before voting. Read from the rendered figure, so it can lag other people's votes by moments.

## FAQ

### What does "Upvote a Product Hunt launch" do?

Upvote a launch on Product Hunt as the signed-in account. Product Hunt's vote control is a toggle, so this script checks whether the account has already upvoted the launch and leaves it alone if so, rather than pressing the control and silently removing an existing vote. The result reports the account that voted, whether the vote was already there, the launch's score afterwards, and confirmation read back from Product Hunt's own response rather than from the button. Accepts a full launch URL or a "product/launch" slug pair. Pair it with the remove-upvote script to undo. Note that Product Hunt votes on a launch, not on a product as a whole: a product with several launches is upvoted one launch at a time.

### How do I automatically upvote a Product Hunt launch on producthunt.com?

Ask an AI agent connected to Reduck to run reduck/producthunt.com/upvote_launch, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/producthunt.com/upvote_launch

### Is there a producthunt.com API to upvote a Product Hunt launch?

You do not need one. "Upvote a Product Hunt launch" drives the real producthunt.com pages in a browser, so it works whether or not producthunt.com offers an API for this.

### What information do I need to provide?

Required: launch.

### What does it return?

It returns postId, hasVoted, launchUrl, scoreAfter, scoreBefore, account_used, already_present, verified_on_page.

### Do I need to be logged in to producthunt.com?

Yes. It acts as you on producthunt.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the producthunt.com cookies saved by the Reduck extension.

### Does it change anything on producthunt.com, or only read data?

It makes changes on producthunt.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/producthunt.com/upvote_launch, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/producthunt.com/upvote_launch

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/producthunt.com/upvote_launch
