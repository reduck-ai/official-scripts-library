# Endorse a skill

Automatically endorse a skill on linkedin.com. Endorse one of a LinkedIn profile's listed skills, by profile URL and the exact skill name shown on their Skills page. Safe to call again on a skill already endorsed by this account — it reports that instead of erroring. Refuses if the profile lists no skills, or the given skill isn't among them.

- Site: linkedin.com
- Address: `reduck/linkedin.com/endorse_skill`
- Updated: 2026-09-18 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/endorse_skill`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/endorse_skill
```

## Input

- `skillName` (string, required): Exact skill name as it appears on their Skills page (e.g. "Adobe InDesign").
- `profileUrl` (string, required): The profile's LinkedIn URL (e.g. https://www.linkedin.com/in/some-public-id/).

## Output

- `status` (string, required)
- `skillName` (string, required)
- `endorsementCount` (integer | null, optional): Total endorsement count for this skill after the action, when shown.

## FAQ

### What does "Endorse a skill" do?

Endorse one of a LinkedIn profile's listed skills, by profile URL and the exact skill name shown on their Skills page. Safe to call again on a skill already endorsed by this account — it reports that instead of erroring. Refuses if the profile lists no skills, or the given skill isn't among them.

### How do I automatically endorse a skill on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/endorse_skill, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/endorse_skill

### Is there a linkedin.com API to endorse a skill?

You do not need one. "Endorse a skill" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: profileUrl, skillName.

### What does it return?

It returns status, skillName, endorsementCount.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/endorse_skill, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/endorse_skill

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/endorse_skill
