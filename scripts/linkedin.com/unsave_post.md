# Unsave LinkedIn post

Automatically unsave LinkedIn post on linkedin.com. Remove a LinkedIn post from your saved items (My Items > Saved posts) by its permalink. Returns not_saved if the post was not in your saved items, or unsaved otherwise, and whether the post's menu showed it as not saved afterwards. A post that was deleted or does not exist fails with a clear error. Pairs with get_saved_posts, which returns each saved post's permalink.

- Site: linkedin.com
- Address: `reduck/linkedin.com/unsave_post`
- Updated: 2026-11-20 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/unsave_post`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/unsave_post
```

## Input

- `postUrl` (string, required): LinkedIn post permalink, e.g. https://www.linkedin.com/feed/update/urn:li:activity:123.../ or https://www.linkedin.com/posts/<slug>. get_saved_posts returns it as postUrl.

## Output

- `status` (string, required): unsaved: the post was in your saved items and was removed. not_saved: it was not saved, so nothing changed.
- `postUrl` (string, required)
- `verified_on_page` (boolean, required): True when the post's menu, opened again after the action, showed the post as not saved.

## FAQ

### What does "Unsave LinkedIn post" do?

Remove a LinkedIn post from your saved items (My Items > Saved posts) by its permalink. Returns not_saved if the post was not in your saved items, or unsaved otherwise, and whether the post's menu showed it as not saved afterwards. A post that was deleted or does not exist fails with a clear error. Pairs with get_saved_posts, which returns each saved post's permalink.

### How do I automatically unsave LinkedIn post on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/unsave_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/unsave_post

### Is there a linkedin.com API to unsave LinkedIn post?

You do not need one. "Unsave LinkedIn post" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: postUrl.

### What does it return?

It returns status, postUrl, verified_on_page.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/unsave_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/unsave_post

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/unsave_post
