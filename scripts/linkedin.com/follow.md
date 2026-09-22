# Follow LinkedIn profile

Automatically follow LinkedIn profile on linkedin.com. Follow a LinkedIn member by profile URL. Works whether Follow is the profile's main button or sits inside the overflow menu, and whatever language the account's interface is set to. Safe to repeat: it returns already_following if you already follow them, and no_follow_cta when the profile offers no Follow option. Also returns the member id it acted on and confirms the resulting state on the page.

- Site: linkedin.com
- Address: `reduck/linkedin.com/follow`
- Updated: 2026-08-26 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/follow`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/follow
```

## Input

- `profileUrl` (string, required): LinkedIn profile URL, e.g. https://www.linkedin.com/in/emmanuelmacron/

## Output

- `status` (string, required): followed = just followed; already_following = you already followed them; no_follow_cta = the profile offers no Follow option.
- `publicId` (string, required): vanity id parsed from the URL (decoded)
- `profileUrl` (string, required)
- `name` (string | null, optional)
- `memberId` (string | null, optional): LinkedIn member id of the profile that was acted on, read from the follow control itself — the join key proving which member the follow applied to. Null only when no Follow option exists.
- `verifiedOnPage` (boolean, optional): True when the follow state was read back from the page after the action (or read directly for already_following), rather than assumed from the click.

## FAQ

### What does "Follow LinkedIn profile" do?

Follow a LinkedIn member by profile URL. Works whether Follow is the profile's main button or sits inside the overflow menu, and whatever language the account's interface is set to. Safe to repeat: it returns already_following if you already follow them, and no_follow_cta when the profile offers no Follow option. Also returns the member id it acted on and confirms the resulting state on the page.

### How do I automatically follow LinkedIn profile on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/follow, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/follow

### Is there a linkedin.com API to follow LinkedIn profile?

You do not need one. "Follow LinkedIn profile" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: profileUrl.

### What does it return?

It returns name, status, memberId, publicId, profileUrl, verifiedOnPage.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/follow, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/follow

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/follow
