# Remove a Product Hunt launch upvote

Automatically remove a Product Hunt launch upvote on producthunt.com. Withdraw the signed-in account's upvote from a Product Hunt launch. This is the inverse of upvoting one, and it is written the same careful way: because Product Hunt's vote control is a toggle, the script first checks whether an upvote actually exists and does nothing if it does not, instead of pressing the control and accidentally adding one. The result reports the account used, whether there was no vote to remove, the score afterwards, and confirmation read back from Product Hunt's own response rather than from the button. Accepts a full launch URL or a "product/launch" slug pair.

- Site: producthunt.com
- Address: `reduck/producthunt.com/remove_launch_upvote`
- Updated: 2026-08-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/producthunt.com/remove_launch_upvote`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/producthunt.com/remove_launch_upvote
```

## Input

- `launch` (string, required): Full launch URL (e.g. "https://www.producthunt.com/products/notion/launches/notion-mail") or a "product/launch" slug pair (e.g. "notion/notion-mail").

## Output

- `hasVoted` (boolean, required): Whether the account still holds an upvote after the run. False on success.
- `launchUrl` (string, required)
- `account_used` (string, required): Handle of the account whose vote was withdrawn, read from the signed-in session rather than assumed.
- `already_absent` (boolean, required): True when this account held no upvote on the launch, so nothing was pressed.
- `verified_on_page` (boolean, required): True when Product Hunt's own response confirmed the launch is no longer upvoted.
- `postId` (string | null, optional): Product Hunt's numeric id for the launch.
- `scoreAfter` (number | null, optional): Score Product Hunt reported with the change. Other people vote continuously, so this is their number at that instant, not necessarily scoreBefore - 1.
- `scoreBefore` (number | null, optional): Score shown on the control before the change. Read from the rendered figure, so it can lag other people's votes by moments.

## FAQ

### What does "Remove a Product Hunt launch upvote" do?

Withdraw the signed-in account's upvote from a Product Hunt launch. This is the inverse of upvoting one, and it is written the same careful way: because Product Hunt's vote control is a toggle, the script first checks whether an upvote actually exists and does nothing if it does not, instead of pressing the control and accidentally adding one. The result reports the account used, whether there was no vote to remove, the score afterwards, and confirmation read back from Product Hunt's own response rather than from the button. Accepts a full launch URL or a "product/launch" slug pair.

### How do I automatically remove a Product Hunt launch upvote on producthunt.com?

Ask an AI agent connected to Reduck to run reduck/producthunt.com/remove_launch_upvote, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/producthunt.com/remove_launch_upvote

### Is there a producthunt.com API to remove a Product Hunt launch upvote?

You do not need one. "Remove a Product Hunt launch upvote" drives the real producthunt.com pages in a browser, so it works whether or not producthunt.com offers an API for this.

### What information do I need to provide?

Required: launch.

### What does it return?

It returns postId, hasVoted, launchUrl, scoreAfter, scoreBefore, account_used, already_absent, verified_on_page.

### Do I need to be logged in to producthunt.com?

Yes. It acts as you on producthunt.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the producthunt.com cookies saved by the Reduck extension.

### Does it change anything on producthunt.com, or only read data?

It makes changes on producthunt.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/producthunt.com/remove_launch_upvote, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/producthunt.com/remove_launch_upvote

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/producthunt.com/remove_launch_upvote
