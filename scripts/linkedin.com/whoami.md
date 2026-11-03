# LinkedIn — who am I

Report which LinkedIn member this browser is signed in as: the username (the vanity slug that other linkedin.com scripts take as publicId), the member's name, the member id, the stable member urn, and whether the account has Premium. When the browser is not signed in to LinkedIn, the run fails with a signed-out error that tells you to sign in to linkedin.com, then retry.

- Site: linkedin.com
- Address: `reduck/linkedin.com/whoami`
- Updated: 2026-11-02 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required): How the verdict was reached, in a short phrase.
- `loggedIn` (boolean, required): Always true: signed out is a SignedOutError.
- `checkedAt` (string, required): ISO timestamp of the check.
- `name` (string | null, optional): firstName + lastName as LinkedIn returns them.
- `userId` (string | null, optional): LinkedIn's numeric member id, as a string.
- `lastName` (string | null, optional)
- `username` (string | null, optional): The member's vanity slug, the part after /in/ in their profile URL. This is the publicId that other linkedin.com scripts take as an argument.
- `firstName` (string | null, optional)
- `memberUrn` (string | null, optional): Stable member urn (urn:li:fs_miniProfile:...). Survives a vanity-slug rename, unlike username, so prefer it as a join key.
- `profileUrl` (string | null, optional): Canonical /in/ URL built from username.
- `premiumSubscriber` (boolean | null, optional): Whether the signed-in member holds a Premium subscription, as LinkedIn reports it. Null when LinkedIn omits the field.

## FAQ

### What does "LinkedIn — who am I" do?

Report which LinkedIn member this browser is signed in as: the username (the vanity slug that other linkedin.com scripts take as publicId), the member's name, the member id, the stable member urn, and whether the account has Premium. When the browser is not signed in to LinkedIn, the run fails with a signed-out error that tells you to sign in to linkedin.com, then retry.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, userId, evidence, lastName, loggedIn, username, checkedAt, firstName, memberUrn, profileUrl, premiumSubscriber.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/whoami
