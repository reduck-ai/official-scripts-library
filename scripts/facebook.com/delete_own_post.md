# Delete your own Facebook post

Automatically delete your own Facebook post on facebook.com. Delete one of your own Facebook posts (typically a group post) from its link, as the signed-in account. Only your own posts can be deleted: on someone else's post the script refuses and says so. Returns deleted once Facebook confirms it and the post is gone, already_gone when the post no longer existed, or not_own_post. To delete several posts, call it once per post. Works in any interface language.

- Site: facebook.com
- Address: `reduck/facebook.com/delete_own_post`
- Updated: 2026-11-13 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/facebook.com/delete_own_post`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/facebook.com/delete_own_post
```

## Input

- `url` (string, required): Link to the post to delete, carrying the post's numeric id, e.g. https://www.facebook.com/groups/<group>/posts/<post>/ (as returned by list_my_posts_in_group).

## Output

- `status` (string, required)

## FAQ

### What does "Delete your own Facebook post" do?

Delete one of your own Facebook posts (typically a group post) from its link, as the signed-in account. Only your own posts can be deleted: on someone else's post the script refuses and says so. Returns deleted once Facebook confirms it and the post is gone, already_gone when the post no longer existed, or not_own_post. To delete several posts, call it once per post. Works in any interface language.

### How do I automatically delete your own Facebook post on facebook.com?

Ask an AI agent connected to Reduck to run reduck/facebook.com/delete_own_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/delete_own_post

### Is there a facebook.com API to delete your own Facebook post?

You do not need one. "Delete your own Facebook post" drives the real facebook.com pages in a browser, so it works whether or not facebook.com offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns status.

### Do I need to be logged in to facebook.com?

Yes. It acts as you on facebook.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the facebook.com cookies saved by the Reduck extension.

### Does it change anything on facebook.com, or only read data?

It makes changes on facebook.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/facebook.com/delete_own_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/delete_own_post

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/facebook.com/delete_own_post
