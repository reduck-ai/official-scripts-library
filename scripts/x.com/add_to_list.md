# Add to X List

Automatically add to X List on x.com. Adds an account to one of this account's X Lists, by exact handle.

- Site: x.com
- Address: `reduck/x.com/add_to_list`
- Updated: 2026-09-08 (v15)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/add_to_list`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/add_to_list
```

## Input

- `handle` (string, required): The account's @handle to add, without the @ (e.g. "MKBHD"). Must be an exact handle - the picker's search is a general people-search, so a partial or display-name query can surface lookalike or parody accounts above the real one.
- `listId` (string, required): The target List's id, from its URL: x.com/i/lists/<listId> (returned by create_list, or visible on any List page).

## Output

- `handle` (string, required)
- `list_id` (string, required)
- `already_member` (boolean, required)
- `member_count_after` (integer, required)
- `member_count_before` (integer, required)

## FAQ

### What does "Add to X List" do?

Adds an account to one of this account's X Lists, by exact handle.

### How do I automatically add to X List on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/add_to_list, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/add_to_list

### Is there a x.com API to add to X List?

You do not need one. "Add to X List" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Required: listId, handle.

### What does it return?

It returns handle, list_id, already_member, member_count_after, member_count_before.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It makes changes on x.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/add_to_list, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/add_to_list

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/add_to_list
