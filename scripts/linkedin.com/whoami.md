# LinkedIn — who am I

Report which LinkedIn member this browser is signed in as: the vanity slug other linkedin.com scripts take as publicId, the member's name, stable member urn, numeric id, and whether the account holds Premium. Being signed out is reported as loggedIn:false with the evidence for that verdict, not as an error, so this can be polled to watch whether a session is still alive. Every verdict carries a timestamp and how it was reached.

- Site: linkedin.com
- Address: `reduck/linkedin.com/whoami`
- Updated: 2026-09-17 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required): How the verdict was reached — e.g. 'voyager /me 200', 'voyager /me 401', 'redirected to …/uas/login', 'no LinkedIn session cookie in this browser'. Present for both verdicts so a false is auditable rather than bare.
- `loggedIn` (boolean, required): True when LinkedIn identified a signed-in member for this browser. False is a real answer, not a failure — it means the session is absent or dead.
- `checkedAt` (string, required): ISO timestamp of the check, so a polled result can be aged.
- `fullName` (string | null, optional): firstName + lastName as LinkedIn returns them; null when signed out.
- `lastName` (string | null, optional)
- `memberId` (number | null, optional): LinkedIn's numeric member id (voyager plainId).
- `firstName` (string | null, optional)
- `memberUrn` (string | null, optional): Stable member urn (urn:li:fs_miniProfile:…). Survives a vanity-slug rename, unlike publicIdentifier, so prefer it as a join key.
- `profileUrl` (string | null, optional): Canonical /in/ URL built from publicIdentifier. Null when signed out.
- `publicIdentifier` (string | null, optional): The member's vanity slug — the part after /in/ in their profile URL. This is the publicId that other linkedin.com scripts take as an argument. Null when signed out.
- `premiumSubscriber` (boolean | null, optional): Whether the signed-in member holds a Premium subscription, as voyager reports it. Null when signed out or when LinkedIn omits the field.

## FAQ

### What does "LinkedIn — who am I" do?

Report which LinkedIn member this browser is signed in as: the vanity slug other linkedin.com scripts take as publicId, the member's name, stable member urn, numeric id, and whether the account holds Premium. Being signed out is reported as loggedIn:false with the evidence for that verdict, not as an error, so this can be polled to watch whether a session is still alive. Every verdict carries a timestamp and how it was reached.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns evidence, fullName, lastName, loggedIn, memberId, checkedAt, firstName, memberUrn, profileUrl, publicIdentifier, premiumSubscriber.

### Do I need to be logged in to linkedin.com?

No. It only uses pages of linkedin.com that are reachable without signing in.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/whoami
