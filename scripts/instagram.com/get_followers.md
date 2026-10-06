# Get Instagram followers

Automatically get Instagram followers on instagram.com. A plain list of who follows an Instagram account, with numeric ids that stay put when a handle changes.

- Site: instagram.com
- Address: `reduck/instagram.com/get_followers`
- Updated: 2026-10-05 (v2)
- Author: Reduck AI (reduck)

## About

The follower pop-up on Instagram is fine for a glance and miserable to copy past a few dozen rows. Give it a handle and a count and it pages through the same list the pop-up loads, 50 accounts per request. Set count to 0 and it keeps going until Instagram stops serving pages. The catch is that it only sees what the Instagram account signed in to that browser sees. That means the full list for that account and for accounts it follows, a short preview anywhere else (has_more goes false early), and nothing from a private account it does not follow. A candle shop that ran a follow-to-enter giveaway, say, pulls its own 1,800 followers with count at 0 and checks the 312 entrant handles against the list before drawing a winner. Bios and follower counts are not included, so run get_profile on the few handles worth a closer look.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/get_followers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_followers
```

## Input

- `username` (string, required): Handle without the @.
- `count` (number, optional): Max followers to fetch; 0 = every page Instagram will serve.

## Output

- `count` (number, required)
- `has_more` (boolean, required): True if Instagram still had pages when we stopped (count reached).
- `username` (string, required)
- `followers` (array, required)

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "count": 3,
  "has_more": true,
  "username": "…",
  "followers": [
    {
      "pk": "…",
      "username": "…",
      "full_name": "…",
      "is_private": true,
      "is_verified": true,
      "profile_pic_url": "https://example.com/item/123"
    }
  ]
}
```

## FAQ

### What does "Get Instagram followers" do?

List an Instagram user's followers by their username. count=0 fetches every page. Instagram serves the full list only to the owner or accounts you follow; for other accounts it returns a capped preview, then has_more flips false. Returns count, has_more, and followers (pk, username, full_name, is_private, is_verified, profile_pic_url).

### How do I automatically get Instagram followers on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_followers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_followers

### Is there a instagram.com API to get Instagram followers?

You do not need one. "Get Instagram followers" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: username. Optional: count.

### What does it return?

It returns count, has_more, username, followers.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It only reads. It looks things up on instagram.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_followers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_followers

### Who maintains it?

It is part of Reduck's official curated catalogue.

### Can I get the complete follower list of a public account I don't follow?

Usually not with this script. On an account you don't follow, the follower endpoint it calls returns a capped preview, and has_more goes false when that preview ends. A private account you don't follow returns no followers at all.

### How do I find out who doesn't follow me back on Instagram?

Run get_followers and get_following on your own username with count set to 0, then list the pk values that appear in following but not in followers. Matching on pk rather than username keeps a renamed account from showing up as a mismatch.

### Is there a limit on how many followers it can export?

On your own account there is no fixed cap: with count 0 it requests 50 followers per page until Instagram stops returning a cursor. If any page fails, the run ends with an error of the form "followers HTTP <status>" and returns nothing. There is no cursor input to resume from, so a retry starts again at page one. If you do not need everyone, a count of 200 is about four requests.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/get_followers
