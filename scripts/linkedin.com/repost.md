# Repost LinkedIn post

Automatically repost LinkedIn post on linkedin.com. Instantly repost a LinkedIn post to your feed by its permalink (no added thoughts). Posts a real repost under the logged-in account. Adding your own commentary via "Repost with your thoughts" isn't supported — this only does the instant repost. If you'd already reposted the post, no duplicate is created and the result reflects that instead. To undo, delete the repost from your own activity (control menu > Delete repost).

- Site: linkedin.com
- Address: `reduck/linkedin.com/repost`
- Updated: 2026-08-24 (v15)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/repost`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/repost
```

## Input

- `postUrl` (string, required): LinkedIn post permalink (/feed/update/urn:li:activity:.../ or /posts/...) to repost.
- `text` (string, optional): Optional commentary. Omit for an instant repost (no commentary). Provide it to use "Repost with your thoughts" -- your text is added above the quoted post. This publishes a real, public repost-with-thoughts under the user's account immediately, so confirm the exact commentary (and each mention) with them before running.
- `mentions` (array, optional): Person or organization names to @mention, appended in order at the end of text (each as ' @Name'); only used with the with-thoughts flow (requires `text`). Confirm each name with the user before running, and ask them to clarify any ambiguous name (e.g. a bare first name) with a full name first. Each name is resolved through the composer's own mention typeahead by an exact, case-insensitive match on the suggestion's primary line -- never guessed from a partial or fuzzy match. If any name has no exact match, or more than one suggestion shares that exact match, nothing is posted and the run throws, naming which mention failed and listing the ambiguous candidates.

## Output

- `postUrl` (string, required): Echoes the permalink of the post that was (or would have been) reposted.
- `reposted` (boolean, required): True once the write went through and created a repost (instant or with-thoughts).
- `account_used` (object, required): The real account the repost was performed under, echoed from the session/UI.
- `alreadyReposted` (boolean, required): True when the instant-repost flow was refused because you'd already instantly reposted this post (LinkedIn blocks duplicate instant reposts per account). Always false for the with-thoughts flow -- LinkedIn allows multiple quote-reposts of the same post.
- `verified_on_page` (boolean, required): True if the script independently reloaded the new repost's own permalink and confirmed it actually renders there (instant repost: a matching feed card; with-thoughts: the commentary text). True on an alreadyReposted hit -- the pre-existing repost was what was matched.
- `url` (string, optional): Permalink of the newly created repost. Absent when alreadyReposted is true (no new repost exists).
- `urn` (string, optional): The new repost's own urn -- urn:li:activity:... for an instant repost, urn:li:share:... for a repost with thoughts. Absent when alreadyReposted is true.

## FAQ

### What does "Repost LinkedIn post" do?

Instantly repost a LinkedIn post to your feed by its permalink (no added thoughts). Posts a real repost under the logged-in account. Adding your own commentary via "Repost with your thoughts" isn't supported — this only does the instant repost. If you'd already reposted the post, no duplicate is created and the result reflects that instead. To undo, delete the repost from your own activity (control menu > Delete repost).

### How do I automatically repost LinkedIn post on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/repost, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/repost

### Is there a linkedin.com API to repost LinkedIn post?

You do not need one. "Repost LinkedIn post" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: postUrl. Optional: text, mentions.

### What does it return?

It returns url, urn, postUrl, reposted, account_used, alreadyReposted, verified_on_page.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/repost, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/repost

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/repost
