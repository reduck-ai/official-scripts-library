# Bulk delete your Facebook group posts

Bulk delete your Facebook group posts by calling this once per post from an agent; Facebook has no bulk delete for group posts. Delete one of your own Facebook posts (typically a group post) from its link. Only your own posts can be deleted — if the post belongs to someone else the script refuses and says so. Returns deleted once the link stops resolving, or already_gone when the post no longer existed.

- Site: facebook.com
- Address: `reduck/facebook.com/delete_own_post`
- Updated: 2026-09-19 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/facebook.com/delete_own_post`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/facebook.com/delete_own_post
```

## Input

- `url` (string, required): Link to the post to delete, e.g. https://www.facebook.com/groups/<group>/posts/<post>/.

## Output

- `status` (string, required)

## FAQ

### What does "Bulk delete your Facebook group posts" do?

Bulk delete your Facebook group posts by calling this once per post from an agent; Facebook has no bulk delete for group posts. Delete one of your own Facebook posts (typically a group post) from its link. Only your own posts can be deleted — if the post belongs to someone else the script refuses and says so. Returns deleted once the link stops resolving, or already_gone when the post no longer existed.

### What information do I need to provide?

Required: url.

### What does it return?

It returns status.

### Do I need to be logged in to facebook.com?

No. It only uses pages of facebook.com that are reachable without signing in.

### Does it change anything on facebook.com, or only read data?

It makes changes on facebook.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/facebook.com/delete_own_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/delete_own_post

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/facebook.com/delete_own_post
