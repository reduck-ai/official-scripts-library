# Set Reddit post flair

Automatically set Reddit post flair on reddit.com. Set or remove the flair on your own Reddit post, by its URL. Picks a matching flair template from the subreddit's own list (filtered by name) and, if the template allows custom text, sets that text; passing an empty flairText removes any existing flair. Returns the flair actually applied, read back from the post. Fails loudly if the subreddit has flair disabled for posts, or if no template matches the requested name.

- Site: reddit.com
- Address: `reduck/reddit.com/set_post_flair`
- Updated: 2026-09-18 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/reddit.com/set_post_flair`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/reddit.com/set_post_flair
```

## Input

- `postUrl` (string, required): URL of the Reddit post to flair (yours, or one you moderate)
- `flairText` (string, optional): Flair text to apply, matched against the subreddit's flair templates. Omit or pass an empty string to remove the post's current flair.

## Output

- `applied` (boolean, required)
- `postUrl` (string, required)
- `flairText` (string | null, optional)
- `verifiedFlair` (string | null, optional): The flair text read back from the post after applying, or null if no flair is set

## FAQ

### What does "Set Reddit post flair" do?

Set or remove the flair on your own Reddit post, by its URL. Picks a matching flair template from the subreddit's own list (filtered by name) and, if the template allows custom text, sets that text; passing an empty flairText removes any existing flair. Returns the flair actually applied, read back from the post. Fails loudly if the subreddit has flair disabled for posts, or if no template matches the requested name.

### How do I automatically set Reddit post flair on reddit.com?

Ask an AI agent connected to Reduck to run reduck/reddit.com/set_post_flair, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/set_post_flair

### Is there a reddit.com API to set Reddit post flair?

You do not need one. "Set Reddit post flair" drives the real reddit.com pages in a browser, so it works whether or not reddit.com offers an API for this.

### What information do I need to provide?

Required: postUrl. Optional: flairText.

### What does it return?

It returns applied, postUrl, flairText, verifiedFlair.

### Do I need to be logged in to reddit.com?

Yes. It acts as you on reddit.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the reddit.com cookies saved by the Reduck extension.

### Does it change anything on reddit.com, or only read data?

It makes changes on reddit.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/reddit.com/set_post_flair, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/set_post_flair

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/reddit.com/set_post_flair
