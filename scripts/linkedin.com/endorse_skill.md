# Endorse a LinkedIn skill

Automatically endorse a LinkedIn skill on linkedin.com. Endorse one of a LinkedIn profile's listed skills, or take back this account's endorsement with remove, by profile URL and the exact skill name shown on their Skills page. Endorsing needs a 1st-degree connection; a profile without the endorse option is refused with a clear message. Safe to call again: a skill already in the requested state returns already_endorsed or not_endorsed instead of clicking. Returns no_skills when the profile lists none and skill_not_found when the skill isn't among them.

- Site: linkedin.com
- Address: `reduck/linkedin.com/endorse_skill`
- Updated: 2026-11-03 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/endorse_skill`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/endorse_skill
```

## Input

- `skillName` (string, required): Exact skill name as it appears on their Skills page (e.g. "Adobe InDesign").
- `profileUrl` (string, required): The profile's LinkedIn URL (e.g. https://www.linkedin.com/in/some-public-id/). Endorsing needs a 1st-degree connection.
- `remove` (boolean, optional): true takes back this account's endorsement of the skill instead of adding one.

## Output

- `status` (string, required)
- `skillName` (string, required)
- `endorsementCount` (integer | null, optional): Endorsement count shown for this skill after the action, null when the profile shows none.

## FAQ

### What does "Endorse a LinkedIn skill" do?

Endorse one of a LinkedIn profile's listed skills, or take back this account's endorsement with remove, by profile URL and the exact skill name shown on their Skills page. Endorsing needs a 1st-degree connection; a profile without the endorse option is refused with a clear message. Safe to call again: a skill already in the requested state returns already_endorsed or not_endorsed instead of clicking. Returns no_skills when the profile lists none and skill_not_found when the skill isn't among them.

### How do I automatically endorse a LinkedIn skill on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/endorse_skill, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/endorse_skill

### Is there a linkedin.com API to endorse a LinkedIn skill?

You do not need one. "Endorse a LinkedIn skill" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: profileUrl, skillName. Optional: remove.

### What does it return?

It returns status, skillName, endorsementCount.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/endorse_skill, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/endorse_skill

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/endorse_skill
