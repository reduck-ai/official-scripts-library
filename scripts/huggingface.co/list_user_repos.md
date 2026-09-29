# Hugging Face — list a user's or org's repos

Automatically list a user's or org's repos on huggingface.co. List the models, datasets and Spaces of a Hugging Face user or organization (e.g. "google", or the username from huggingface.co/whoami): each repo's type, id, URL, likes, downloads, private flag, pipeline tag (models), SDK (Spaces) and last-modified date, most downloaded / liked first. Pick which types to list and how many per type. Public repos need no sign-in; when signed in, the account's own private repos are included. An author with no repos returns an empty list.

- Site: huggingface.co
- Address: `reduck/huggingface.co/list_user_repos`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/huggingface.co/list_user_repos`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/huggingface.co/list_user_repos
```

## Input

- `author` (string, required): Hub user or organization name, e.g. "google" or the username from huggingface.co/whoami.
- `limit` (integer, optional): Maximum repos per type (default 20), most downloaded / liked first.
- `types` (array, optional): Which repo types to list (default all three).

## Output

- `repos` (array, required)
- `author` (string, required)
- `counts` (object, optional)

## FAQ

### What does "Hugging Face — list a user's or org's repos" do?

List the models, datasets and Spaces of a Hugging Face user or organization (e.g. "google", or the username from huggingface.co/whoami): each repo's type, id, URL, likes, downloads, private flag, pipeline tag (models), SDK (Spaces) and last-modified date, most downloaded / liked first. Pick which types to list and how many per type. Public repos need no sign-in; when signed in, the account's own private repos are included. An author with no repos returns an empty list.

### How do I automatically list a user's or org's repos on huggingface.co?

Ask an AI agent connected to Reduck to run reduck/huggingface.co/list_user_repos, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/huggingface.co/list_user_repos

### Is there a huggingface.co API to list a user's or org's repos?

You do not need one. "Hugging Face — list a user's or org's repos" drives the real huggingface.co pages in a browser, so it works whether or not huggingface.co offers an API for this.

### What information do I need to provide?

Required: author. Optional: limit, types.

### What does it return?

It returns repos, author, counts.

### Do I need to be logged in to huggingface.co?

No. It only uses pages of huggingface.co that are reachable without signing in.

### Does it change anything on huggingface.co, or only read data?

It only reads. It looks things up on huggingface.co and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/huggingface.co/list_user_repos, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/huggingface.co/list_user_repos

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/huggingface.co/list_user_repos
