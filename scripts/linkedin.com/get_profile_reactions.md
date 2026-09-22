# Get LinkedIn profile reactions

Automatically get LinkedIn profile reactions on linkedin.com. Get the posts a LinkedIn profile has reacted to (liked, loved, etc.), from its Reactions activity feed by public ID, scrolling to load up to count reactions. Returns each reaction's type as LinkedIn phrases it (in the profile's display language) plus the reacted-to post (author, headline, text, age, permalink). Complements the profile posts and comments activity scripts.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_profile_reactions`
- Updated: 2026-09-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_profile_reactions`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_profile_reactions
```

## Input

- `publicId` (string, required): LinkedIn public profile ID — the slug in linkedin.com/in/<publicId>/ (e.g. 'peter-csiba').
- `count` (integer, optional): Max number of reactions to collect by scrolling the Reactions activity feed. Default 10; the feed may return fewer if exhausted.

## Output

- `reactions` (array, required)

## FAQ

### What does "Get LinkedIn profile reactions" do?

Get the posts a LinkedIn profile has reacted to (liked, loved, etc.), from its Reactions activity feed by public ID, scrolling to load up to count reactions. Returns each reaction's type as LinkedIn phrases it (in the profile's display language) plus the reacted-to post (author, headline, text, age, permalink). Complements the profile posts and comments activity scripts.

### How do I automatically get LinkedIn profile reactions on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_profile_reactions, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_profile_reactions

### Is there a linkedin.com API to get LinkedIn profile reactions?

You do not need one. "Get LinkedIn profile reactions" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: publicId. Optional: count.

### What does it return?

It returns reactions.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_profile_reactions, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_profile_reactions

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_profile_reactions
