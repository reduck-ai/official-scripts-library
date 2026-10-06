# Upvote a Product Hunt launch

Automatically upvote a Product Hunt launch on producthunt.com. Casts one vote on a launch only if the account has not voted yet, and reports the score.

- Site: producthunt.com
- Address: `reduck/producthunt.com/upvote_launch`
- Updated: 2026-10-05 (v1)
- Author: Reduck AI (reduck)

## About

Product Hunt's upvote button is a toggle. Press it on a launch you already backed from your phone and you have quietly taken that vote back, which is the classic way an agent doing the clicking gets this wrong. So the run reads the vote icon first and presses only when it is empty. Say you keep a list of tools you tried this month, notion/notion-mail among them, and have your agent back each one from your own account. That is one run per launch. already_present comes back true for the ones you had voted on before, and scoreAfter carries the total Product Hunt returned with your vote, which can differ from scoreBefore plus one because other people vote at the same time. The check rests on the filled icon the site draws today, so a redesign can mean errors, or at worst a press that undoes an existing vote before the run reports the failure.

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

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "postId": "abc123",
  "hasVoted": true,
  "launchUrl": "https://example.com/item/123",
  "scoreAfter": 3.5,
  "scoreBefore": 3.5,
  "account_used": "…",
  "already_present": true,
  "verified_on_page": true
}
```

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

It makes changes on producthunt.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/producthunt.com/upvote_launch, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/producthunt.com/upvote_launch

### Who maintains it?

It is part of Reduck's official curated catalogue.

### What happens if Product Hunt redesigns its upvote button?

The run decides whether you have already voted by reading the filled icon on Product Hunt's vote button, so a redesign is its weak point. If the icon cannot be read, the run stops with an error before pressing anything. If the icon changes in a way the check misreads, the press can undo an existing vote, and the run then fails because Product Hunt's reply shows the launch is not upvoted.

### Why is my Product Hunt link rejected?

Links in the /posts/notion-mail or /products/notion?launch=notion-mail form are rejected with a message that no product and launch could be read. Rewrite them as notion/notion-mail, or as https://www.producthunt.com/products/notion/launches/notion-mail. The launch slug is the part after /launches/ in the address bar.

### Can it list the people who upvoted a launch?

It casts your own vote and reports the launch's score before and after. It never reads who else voted, so there is no voter list in the result, only the two score figures and the account that voted.

### Why is scoreAfter not exactly scoreBefore plus one?

scoreBefore is read from the figure rendered on the vote button, and scoreAfter is the score Product Hunt returned with your vote. Other people vote continuously, so the two numbers can differ by more than your own vote.

Source: https://reduck.ai/explore/scripts/reduck/producthunt.com/upvote_launch
