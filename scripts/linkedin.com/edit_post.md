# Edit LinkedIn post

Automatically edit LinkedIn post on linkedin.com. Edit the text of one of your own LinkedIn posts, given its permalink. Replaces the body with new text and confirms the change actually rendered on the post afterwards. Refuses posts you cannot edit (someone else's, or a type LinkedIn offers no Edit action for) instead of guessing.

- Site: linkedin.com
- Address: `reduck/linkedin.com/edit_post`
- Updated: 2026-09-03 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/edit_post`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/edit_post
```

## Input

- `url` (string, required): Permalink of a post owned by the logged-in account, e.g. https://www.linkedin.com/feed/update/urn:li:share:7498370628849147904/ — as returned by create_post, get_post or get_profile_posts. Query string is ignored. A post belonging to someone else is refused, since LinkedIn offers no Edit action on it.
- `text` (string, required): The new post body, replacing the existing one entirely. This edits a real, public post immediately and irreversibly — the previous text is not recoverable through this script — so show the exact replacement text to the user and get their explicit approval for this specific content before running. Approval from an earlier or unrelated message does not carry over. LinkedIn publicly marks an edited post as edited.

## Output

- `url` (string, required): The permalink acted on, query string stripped.
- `text` (string, required): The new body that was saved.
- `edited` (boolean, required): True once the Save went through.
- `account_used` (string | null, required): Display name of the logged-in member, read from the post's own author line rather than assumed.
- `verified_on_page` (boolean, required): True only if the permalink was reloaded after saving and the post actually renders the new text. Never inferred from the dialog closing.
- `unchanged` (boolean, optional): True when the requested text already matched the post's current body — nothing was saved, because LinkedIn keeps Save disabled until the text actually differs.
- `previous_text` (string | null, optional): The body as it stood before this edit, read out of the editor. Null if it could not be read.

## FAQ

### What does "Edit LinkedIn post" do?

Edit the text of one of your own LinkedIn posts, given its permalink. Replaces the body with new text and confirms the change actually rendered on the post afterwards. Refuses posts you cannot edit (someone else's, or a type LinkedIn offers no Edit action for) instead of guessing.

### How do I automatically edit LinkedIn post on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/edit_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/edit_post

### Is there a linkedin.com API to edit LinkedIn post?

You do not need one. "Edit LinkedIn post" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: url, text.

### What does it return?

It returns url, text, edited, unchanged, account_used, previous_text, verified_on_page.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/edit_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/edit_post

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/edit_post
