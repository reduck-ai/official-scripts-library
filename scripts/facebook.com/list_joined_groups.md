# Export the list of Facebook groups you're in

Automatically export the list of Facebook groups you're in on facebook.com. Export the list of Facebook groups you are a member of without waiting for Facebook's Download Your Information archive. List the Facebook groups you belong to, and separately the ones you asked to join and are still waiting on. Each entry gives the group's id, link, name, and the line the page shows beneath it — when you last visited for a membership, how long ago the request was sent for a pending one. The counts Facebook displays come back too, so you can tell a capped read from a complete one. Handy for auditing a large account, or for spotting join requests that have been waiting too long.

- Site: facebook.com
- Address: `reduck/facebook.com/list_joined_groups`
- Updated: 2026-09-19 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/facebook.com/list_joined_groups`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/facebook.com/list_joined_groups
```

## Input

- `limit` (integer, optional): Max joined groups to return; the list is infinite-scroll and the script scrolls until it has this many or the list stops growing. Pending requests are always returned in full.

## Output

- `groups` (array, required): Groups the account is actually a member of.
- `totalDeclared` (integer | null, required): Membership count as displayed. groups.length < totalDeclared means the read was capped by limit or by the feed.
- `pendingRequests` (array, required): Groups the account asked to join and is still waiting on — not memberships.
- `pendingDeclared` (integer | null, optional): Pending-request count as displayed.

## FAQ

### What does "Export the list of Facebook groups you're in" do?

Export the list of Facebook groups you are a member of without waiting for Facebook's Download Your Information archive. List the Facebook groups you belong to, and separately the ones you asked to join and are still waiting on. Each entry gives the group's id, link, name, and the line the page shows beneath it — when you last visited for a membership, how long ago the request was sent for a pending one. The counts Facebook displays come back too, so you can tell a capped read from a complete one. Handy for auditing a large account, or for spotting join requests that have been waiting too long.

### How do I automatically export the list of Facebook groups you're in on facebook.com?

Ask an AI agent connected to Reduck to run reduck/facebook.com/list_joined_groups, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/list_joined_groups

### Is there a facebook.com API to export the list of Facebook groups you're in?

You do not need one. "Export the list of Facebook groups you're in" drives the real facebook.com pages in a browser, so it works whether or not facebook.com offers an API for this.

### What information do I need to provide?

Optional: limit.

### What does it return?

It returns groups, totalDeclared, pendingDeclared, pendingRequests.

### Do I need to be logged in to facebook.com?

Yes. It acts as you on facebook.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the facebook.com cookies saved by the Reduck extension.

### Does it change anything on facebook.com, or only read data?

It only reads. It looks things up on facebook.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/facebook.com/list_joined_groups, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/list_joined_groups

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/facebook.com/list_joined_groups
