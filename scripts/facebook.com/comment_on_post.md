# Comment on a Facebook post

Automatically comment on a Facebook post on facebook.com. Leave a comment on a Facebook post, as the identity the browser is currently signed in as. Pass the post's URL and the comment text. If a comment with exactly the same text is already loaded on the post, nothing is posted again. After posting, the comment is looked up on the page to confirm it is really visible, and the account that posted it is echoed back so you can tell which identity was used. Works in any interface language.

- Site: facebook.com
- Address: `reduck/facebook.com/comment_on_post`
- Updated: 2026-11-13 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/facebook.com/comment_on_post`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/facebook.com/comment_on_post
```

## Input

- `text` (string, required): The comment text to publish
- `postUrl` (string, required): Full URL of the Facebook post to comment on

## Output

- `posted` (boolean, required)
- `accountId` (string, required): Numeric id of the identity that published, read from the live session
- `commentUrl` (string | null, required): Link to the comment itself: the one just posted, or the identical comment or reply that was already there.
- `alreadyPresent` (boolean, required): A comment or a reply with this text was already loaded on the post, so nothing was published
- `verifiedOnPage` (boolean, required): The comment was found on the page after publishing
- `text` (string, optional)

## FAQ

### What does "Comment on a Facebook post" do?

Leave a comment on a Facebook post, as the identity the browser is currently signed in as. Pass the post's URL and the comment text. If a comment with exactly the same text is already loaded on the post, nothing is posted again. After posting, the comment is looked up on the page to confirm it is really visible, and the account that posted it is echoed back so you can tell which identity was used. Works in any interface language.

### How do I automatically comment on a Facebook post on facebook.com?

Ask an AI agent connected to Reduck to run reduck/facebook.com/comment_on_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/comment_on_post

### Is there a facebook.com API to comment on a Facebook post?

You do not need one. "Comment on a Facebook post" drives the real facebook.com pages in a browser, so it works whether or not facebook.com offers an API for this.

### What information do I need to provide?

Required: postUrl, text.

### What does it return?

It returns text, posted, accountId, commentUrl, alreadyPresent, verifiedOnPage.

### Do I need to be logged in to facebook.com?

Yes. It acts as you on facebook.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the facebook.com cookies saved by the Reduck extension.

### Does it change anything on facebook.com, or only read data?

It makes changes on facebook.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/facebook.com/comment_on_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/comment_on_post

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/facebook.com/comment_on_post
