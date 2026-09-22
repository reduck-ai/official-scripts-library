# Unfollow LinkedIn profile

Automatically unfollow LinkedIn profile on linkedin.com. Unfollow a LinkedIn member by profile URL. Handles the primary "Following" toggle (pro/creator profiles) and the three-dot "Unfollow" item (normal profiles); confirms the "Unfollow <name>?" dialog. Safe to repeat: it returns not_following if you don't follow them. Statuses: unfollowed/not_following.

- Site: linkedin.com
- Address: `reduck/linkedin.com/unfollow`
- Updated: 2026-08-26 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/unfollow`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/unfollow
```

## Input

- `profileUrl` (string, required): LinkedIn profile URL, e.g. https://www.linkedin.com/in/emmanuelmacron/

## Output

- `status` (string, required): unfollowed = just unfollowed; not_following = a follow control exists and shows you don't follow them; no_follow_cta = the profile offers no follow/unfollow control at all.
- `publicId` (string, required): vanity id parsed from the URL (decoded)
- `profileUrl` (string, required)
- `name` (string | null, optional)
- `memberId` (string | null, optional): LinkedIn member id of the profile acted on, read from the follow control itself. Null only when no follow control exists (no_follow_cta).
- `verifiedOnPage` (boolean, optional): True when the resulting state was read back from the page after the action (or read directly for not_following), rather than assumed from the click.

## FAQ

### What does "Unfollow LinkedIn profile" do?

Unfollow a LinkedIn member by profile URL. Handles the primary "Following" toggle (pro/creator profiles) and the three-dot "Unfollow" item (normal profiles); confirms the "Unfollow <name>?" dialog. Safe to repeat: it returns not_following if you don't follow them. Statuses: unfollowed/not_following.

### How do I automatically unfollow LinkedIn profile on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/unfollow, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/unfollow

### Is there a linkedin.com API to unfollow LinkedIn profile?

You do not need one. "Unfollow LinkedIn profile" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: profileUrl.

### What does it return?

It returns name, status, memberId, publicId, profileUrl, verifiedOnPage.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/unfollow, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/unfollow

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/unfollow
