# Get Instagram following

Automatically get Instagram following on instagram.com. List the accounts an Instagram user follows, by their username, one page per run. Returns username, count, has_more, next_cursor and following (pk, username, full_name, is_private, is_verified, profile_pic_url). To read the next page, run it again with cursor set to next_cursor; has_more is false and next_cursor null on the last page. A username that does not exist, or a private account this account does not follow, fails with an error that says so.

- Site: instagram.com
- Address: `reduck/instagram.com/get_following`
- Updated: 2026-11-11 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/get_following`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_following
```

## Input

- `username` (string, required): Instagram username without the @, e.g. "nasa"
- `cursor` (string, optional): next_cursor of the previous page. Omit it for the first page.

## Output

- `count` (integer, required): Number of accounts on this page.
- `has_more` (boolean, required): True when another page can be read with next_cursor.
- `username` (string, required)
- `following` (array, required)
- `next_cursor` (string | null, required): Pass it as cursor to read the next page. Null on the last page.

## FAQ

### What does "Get Instagram following" do?

List the accounts an Instagram user follows, by their username, one page per run. Returns username, count, has_more, next_cursor and following (pk, username, full_name, is_private, is_verified, profile_pic_url). To read the next page, run it again with cursor set to next_cursor; has_more is false and next_cursor null on the last page. A username that does not exist, or a private account this account does not follow, fails with an error that says so.

### How do I automatically get Instagram following on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_following, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_following

### Is there a instagram.com API to get Instagram following?

You do not need one. "Get Instagram following" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: username. Optional: cursor.

### What does it return?

It returns count, has_more, username, following, next_cursor.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It only reads. It looks things up on instagram.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_following, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_following

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/get_following
