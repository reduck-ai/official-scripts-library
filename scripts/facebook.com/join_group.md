# Join Facebook groups automatically

Automatically join Facebook groups automatically on facebook.com. Join Facebook groups automatically from an agent, one group per call, including private groups with entry questions. Join a Facebook group by id/slug. Returns status (joined / pending / already_member) and name. Pending means a private-group request was sent, not membership.

- Site: facebook.com
- Address: `reduck/facebook.com/join_group`
- Updated: 2026-09-19 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/facebook.com/join_group`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/facebook.com/join_group
```

## Input

- `groupId` (string, required): Numeric id or vanity slug from a group URL (the part after /groups/).
- `answers` (array, optional): Optional answers to a private group's entry questions, in the order the dialog shows them. Extra answers are ignored; missing ones leave their field empty.

## Output

- `name` (string | null, optional)
- `status` (string, optional)
- `groupId` (string, optional)

## FAQ

### What does "Join Facebook groups automatically" do?

Join Facebook groups automatically from an agent, one group per call, including private groups with entry questions. Join a Facebook group by id/slug. Returns status (joined / pending / already_member) and name. Pending means a private-group request was sent, not membership.

### How do I automatically join Facebook groups automatically on facebook.com?

Ask an AI agent connected to Reduck to run reduck/facebook.com/join_group, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/join_group

### Is there a facebook.com API to join Facebook groups automatically?

You do not need one. "Join Facebook groups automatically" drives the real facebook.com pages in a browser, so it works whether or not facebook.com offers an API for this.

### What information do I need to provide?

Required: groupId. Optional: answers.

### What does it return?

It returns name, status, groupId.

### Do I need to be logged in to facebook.com?

No. It only uses pages of facebook.com that are reachable without signing in.

### Does it change anything on facebook.com, or only read data?

It makes changes on facebook.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/facebook.com/join_group, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/join_group

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/facebook.com/join_group
