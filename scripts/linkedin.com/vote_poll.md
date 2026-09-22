# vote_poll

Vote in a LinkedIn poll post by its permalink and the option text to select. Your vote is visible to the poll's author and, depending on the poll's settings, to other voters. Returns the options as the poll lists them, which one was selected, and the vote counts/percentages after voting. Voting is permanent — LinkedIn gives no way to change or retract a poll vote once cast.

- Site: linkedin.com
- Address: `reduck/linkedin.com/vote_poll`
- Updated: 2026-09-03 (v21)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/vote_poll`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/vote_poll
```

## Input

- `option` (string, required): The exact text of the option to vote for, matched against the poll's own option list.
- `postUrl` (string, required): The poll post's permalink, e.g. from linkedin.com/search_posts or linkedin.com/get_post.

## Output

- `voted` (boolean, required)
- `options` (array, required)
- `already_voted` (boolean, required): True when the account had already voted in this poll before this call - LinkedIn does not allow changing a vote through this flow (an Undo affordance exists separately, out of scope).
- `selectedOption` (string | null, optional)

## FAQ

### What does "vote_poll" do?

Vote in a LinkedIn poll post by its permalink and the option text to select. Your vote is visible to the poll's author and, depending on the poll's settings, to other voters. Returns the options as the poll lists them, which one was selected, and the vote counts/percentages after voting. Voting is permanent — LinkedIn gives no way to change or retract a poll vote once cast.

### What information do I need to provide?

Required: postUrl, option.

### What does it return?

It returns voted, options, already_voted, selectedOption.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/vote_poll, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/vote_poll

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/vote_poll
