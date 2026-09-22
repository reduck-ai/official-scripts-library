# Leave multiple Facebook groups at once

Automatically leave multiple Facebook groups at once on facebook.com. Leave several Facebook groups at once by calling this once per group from an agent, instead of clicking through each one. Leave a Facebook group, or withdraw a pending join request, as the signed-in identity. Pass the group's id, short name or URL. Returns what actually happened: left, request_cancelled, not_member (you weren't a member — nothing to do), or unavailable (the group no longer exists or your account cannot see it).

- Site: facebook.com
- Address: `reduck/facebook.com/leave_group`
- Updated: 2026-09-19 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/facebook.com/leave_group`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/facebook.com/leave_group
```

## Input

- `group` (string, required): Group id or short name as in the group URL, or the full group URL.

## Output

- `status` (string, required)
- `name` (string | null, optional): Group display name when readable

## FAQ

### What does "Leave multiple Facebook groups at once" do?

Leave several Facebook groups at once by calling this once per group from an agent, instead of clicking through each one. Leave a Facebook group, or withdraw a pending join request, as the signed-in identity. Pass the group's id, short name or URL. Returns what actually happened: left, request_cancelled, not_member (you weren't a member — nothing to do), or unavailable (the group no longer exists or your account cannot see it).

### How do I automatically leave multiple Facebook groups at once on facebook.com?

Ask an AI agent connected to Reduck to run reduck/facebook.com/leave_group, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/leave_group

### Is there a facebook.com API to leave multiple Facebook groups at once?

You do not need one. "Leave multiple Facebook groups at once" drives the real facebook.com pages in a browser, so it works whether or not facebook.com offers an API for this.

### What information do I need to provide?

Required: group.

### What does it return?

It returns name, status.

### Do I need to be logged in to facebook.com?

Yes. It acts as you on facebook.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the facebook.com cookies saved by the Reduck extension.

### Does it change anything on facebook.com, or only read data?

It makes changes on facebook.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/facebook.com/leave_group, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/leave_group

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/facebook.com/leave_group
