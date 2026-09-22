# Get LinkedIn profile skills

Automatically get LinkedIn profile skills on linkedin.com. Get the full list of skills a LinkedIn profile lists, in the order the profile shows them, from the profile's own skills page. Pass the public profile id or a full profile URL. Each skill comes with the supporting lines shown beneath it — the jobs, schools and certifications it is tied to, plus any endorsement or skill-assessment note — and, where the profile offers them, a link to the skill's endorsers list and a link to its detail page. Both links are per-skill rather than per-profile: most skills carry neither, a skill with endorsements usually carries the endorsers one, and only a skill with more detail than fits inline carries the detail one, so expect null on many entries. Profiles that list no skills come back as an empty list rather than an error. Requires being logged in to LinkedIn. Complements the profile experience and education scripts.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_profile_skills`
- Updated: 2026-09-03 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_profile_skills`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_profile_skills
```

## Input

- `publicId` (string, required): LinkedIn public profile id (the part after /in/ in the profile URL). A full profile URL is also accepted.

## Output

- `count` (integer, required): Number of skills returned; 0 when the profile lists none.
- `skills` (array, required)
- `publicId` (string, required)
- `profileUrl` (string, required)

## FAQ

### What does "Get LinkedIn profile skills" do?

Get the full list of skills a LinkedIn profile lists, in the order the profile shows them, from the profile's own skills page. Pass the public profile id or a full profile URL. Each skill comes with the supporting lines shown beneath it — the jobs, schools and certifications it is tied to, plus any endorsement or skill-assessment note — and, where the profile offers them, a link to the skill's endorsers list and a link to its detail page. Both links are per-skill rather than per-profile: most skills carry neither, a skill with endorsements usually carries the endorsers one, and only a skill with more detail than fits inline carries the detail one, so expect null on many entries. Profiles that list no skills come back as an empty list rather than an error. Requires being logged in to LinkedIn. Complements the profile experience and education scripts.

### How do I automatically get LinkedIn profile skills on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_profile_skills, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_profile_skills

### Is there a linkedin.com API to get LinkedIn profile skills?

You do not need one. "Get LinkedIn profile skills" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: publicId.

### What does it return?

It returns count, skills, publicId, profileUrl.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_profile_skills, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_profile_skills

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_profile_skills
