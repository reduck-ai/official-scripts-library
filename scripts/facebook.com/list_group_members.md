# Export a Facebook group member list

Automatically export a Facebook group member list on facebook.com. Export the member list of a Facebook group as structured data, the CSV-style export Facebook itself does not offer. List members of a Facebook group with name, userId, profileUrl, and a subtitle (role like "Admin", bio, mutual-friends, or join-recency line as Facebook shows it). Order follows Facebook's own members view (admins and group contributors, then recent members), so it doubles as a "who's active / who to connect with" surface. Subtitle varies per row (role, bio, or "Membre depuis..."); results are infinite-scroll, capped by limit.

- Site: facebook.com
- Address: `reduck/facebook.com/list_group_members`
- Updated: 2026-09-19 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/facebook.com/list_group_members`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/facebook.com/list_group_members
```

## Input

- `groupId` (string, required): Numeric id or vanity slug from a group URL (the part after /groups/).
- `limit` (integer, optional): Max members to return. Members list is infinite-scroll; the script scrolls (arming a GraphQL wait before each scroll) until it has this many or the list stops growing.

## FAQ

### What does "Export a Facebook group member list" do?

Export the member list of a Facebook group as structured data, the CSV-style export Facebook itself does not offer. List members of a Facebook group with name, userId, profileUrl, and a subtitle (role like "Admin", bio, mutual-friends, or join-recency line as Facebook shows it). Order follows Facebook's own members view (admins and group contributors, then recent members), so it doubles as a "who's active / who to connect with" surface. Subtitle varies per row (role, bio, or "Membre depuis..."); results are infinite-scroll, capped by limit.

### How do I automatically export a Facebook group member list on facebook.com?

Ask an AI agent connected to Reduck to run reduck/facebook.com/list_group_members, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/list_group_members

### Is there a facebook.com API to export a Facebook group member list?

You do not need one. "Export a Facebook group member list" drives the real facebook.com pages in a browser, so it works whether or not facebook.com offers an API for this.

### What information do I need to provide?

Required: groupId. Optional: limit.

### Do I need to be logged in to facebook.com?

Yes. It acts as you on facebook.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the facebook.com cookies saved by the Reduck extension.

### Does it change anything on facebook.com, or only read data?

It only reads. It looks things up on facebook.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/facebook.com/list_group_members, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/list_group_members

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/facebook.com/list_group_members
