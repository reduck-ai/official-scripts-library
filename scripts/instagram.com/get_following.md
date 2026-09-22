# Get Instagram following

Automatically get Instagram following on instagram.com. List the accounts an Instagram user follows by their username. count=0 fetches every page. Returns count, has_more, and following (pk, username, full_name, is_private, is_verified, profile_pic_url). You'll get the complete list only for your own account or accounts you follow; for anyone else Instagram serves a limited preview.

- Site: instagram.com
- Address: `reduck/instagram.com/get_following`
- Updated: 2026-09-03 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/get_following`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_following
```

## Input

- `username` (string, required): Handle without the @.
- `count` (number, optional): Max accounts to fetch; 0 = every page Instagram will serve.

## Output

- `count` (number, required)
- `has_more` (boolean, required): True if Instagram still had pages when we stopped (count reached).
- `username` (string, required)
- `following` (array, required)

## FAQ

### What does "Get Instagram following" do?

List the accounts an Instagram user follows by their username. count=0 fetches every page. Returns count, has_more, and following (pk, username, full_name, is_private, is_verified, profile_pic_url). You'll get the complete list only for your own account or accounts you follow; for anyone else Instagram serves a limited preview.

### How do I automatically get Instagram following on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_following, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_following

### Is there a instagram.com API to get Instagram following?

You do not need one. "Get Instagram following" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: username. Optional: count.

### What does it return?

It returns count, has_more, username, following.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It only reads. It looks things up on instagram.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_following, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_following

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/get_following
