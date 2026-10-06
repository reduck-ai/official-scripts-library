# Unblock Instagram user

Automatically unblock Instagram user on instagram.com. Lets that account see your posts and stories and message you again, though old follows stay gone.

- Site: instagram.com
- Address: `reduck/instagram.com/unblock_user`
- Updated: 2026-10-05 (v3)
- Author: Reduck AI (reduck)

## About

For one account, tapping Unblock on the profile in the app is still quicker. An agent earns its keep when the unblock is one step in a longer job or there is a list to get through. Say a ceramics shop blocked a customer in the middle of a refund argument. The refund got settled by email, and now the owner wants that customer to see Friday's restock story, which a blocked account cannot. The agent passes the handle without the @, and the run checks Instagram's own profile data to confirm the block exists before clicking Unblock and the confirm button. Getting the customer back as a follower is their call, since unblocking does not restore the follow the block removed. If the account is not blocked, no longer exists or is your own, the run stops before clicking anything. The button is found by its label, tested in English, French, German, Italian and Spanish.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/unblock_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/unblock_user
```

## Input

- `username` (string, required): Instagram handle without @, e.g. natgeo

## Output

- `user_id` (string, required)
- `blocking` (boolean, required): False once unblock succeeds.
- `username` (string, required)

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "user_id": "abc123",
  "blocking": true,
  "username": "…"
}
```

## FAQ

### What does "Unblock Instagram user" do?

Unblock an Instagram user from their profile. Fails loudly if the profile doesn't render an Unblock button (i.e. they weren't blocked). Returns username, user_id, and blocking.

### How do I automatically unblock Instagram user on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/unblock_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/unblock_user

### Is there a instagram.com API to unblock Instagram user?

You do not need one. "Unblock Instagram user" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: username.

### What does it return?

It returns user_id, blocking, username.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It makes changes on instagram.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/unblock_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/unblock_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

### Can it unblock me from someone who blocked my Instagram account?

No. It only lifts a block that you placed on another account, and a block someone else put on you can only be removed by that person. It also does nothing about Instagram itself being blocked on a school or office network.

### Can I unblock all my blocked Instagram accounts at once?

Not in one run. Each run takes a single handle, so a bulk unblock means an agent looping over a list whose names you copy from Blocked accounts in Instagram's settings, since no Reduck script reads that list for you. A handle typed from memory that the person has since changed fails, either as profile not found or, if someone else took the name, as not currently blocked.

### Will the person follow me again after I unblock them on Instagram?

No. A block drops any follow between you, unblocking does not restore it, and Instagram does not tell the person they were unblocked, so they would have to follow you again on their own. If you want to follow them yourself, follow_user does that on the same handle.

### Does it work if my Instagram is set to Dutch or Japanese?

The block check reads Instagram's data and works in any language, but the Unblock button is found by its label, tested in English, French, German, Italian and Spanish (Portuguese uses the same Desbloquear label as Spanish, so it should match, though it was not tested). On any other language the run stops at the button without changing anything, so either tap Unblock yourself or switch the account to English with switch_language first and back afterwards.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/unblock_user
