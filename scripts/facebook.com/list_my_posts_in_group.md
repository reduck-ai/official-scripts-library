# List my Facebook posts in a group

Automatically list my Facebook posts in a group on facebook.com. List your own posts in one Facebook group, with each post's moderation status: pending admin approval, published, declined, or removed. This is how you check whether a post you submitted was accepted, without scrolling the group feed. Reflects the identity the browser is currently acting as.

- Site: facebook.com
- Address: `reduck/facebook.com/list_my_posts_in_group`
- Updated: 2026-11-13 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/facebook.com/list_my_posts_in_group`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/facebook.com/list_my_posts_in_group
```

## Input

- `group` (string, required): Group id or vanity slug as it appears in the group URL (e.g. 77982072346 or decoetbrico), or the full group URL.
- `tabs` (array, optional): Which statuses to read (the tabs of the group's "your content" area). A tab the group does not offer to you, such as pending or declined in a group you administer, has nothing to list.

## Output

- `posts` (array, required)
- `groupUrl` (string, required)

## FAQ

### What does "List my Facebook posts in a group" do?

List your own posts in one Facebook group, with each post's moderation status: pending admin approval, published, declined, or removed. This is how you check whether a post you submitted was accepted, without scrolling the group feed. Reflects the identity the browser is currently acting as.

### How do I automatically list my Facebook posts in a group on facebook.com?

Ask an AI agent connected to Reduck to run reduck/facebook.com/list_my_posts_in_group, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/list_my_posts_in_group

### Is there a facebook.com API to list my Facebook posts in a group?

You do not need one. "List my Facebook posts in a group" drives the real facebook.com pages in a browser, so it works whether or not facebook.com offers an API for this.

### What information do I need to provide?

Required: group. Optional: tabs.

### What does it return?

It returns posts, groupUrl.

### Do I need to be logged in to facebook.com?

Yes. It acts as you on facebook.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the facebook.com cookies saved by the Reduck extension.

### Does it change anything on facebook.com, or only read data?

It only reads. It looks things up on facebook.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/facebook.com/list_my_posts_in_group, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/list_my_posts_in_group

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/facebook.com/list_my_posts_in_group
