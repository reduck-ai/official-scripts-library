# Post to a Facebook group without the Groups API

Automatically post to a Facebook group without the Groups API on facebook.com. Publish to Facebook groups from an agent without Graph API group posting permissions, which Meta removed in v19: this acts as the signed-in member, so it needs no app review. Publish a post to a Facebook group, optionally with a photo (imageUrl fetched in-page, or imageBase64). Works on discussion and buy/sell groups. Returns posted, photoAttached, and verified — the post is looked up on the group's "your content" page after publishing, so verified:false flags posts held for admin approval. dryRun arms the composer without publishing.

- Site: facebook.com
- Address: `reduck/facebook.com/post_to_group`
- Updated: 2026-09-19 (v14)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/facebook.com/post_to_group`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/facebook.com/post_to_group
```

## Input

- `groupId` (string, required): Numeric id or vanity slug from a group URL (the part after /groups/). You must be a member / allowed to post; some groups hold posts for admin approval.
- `message` (string, required): Plain-text post body.
- `dryRun` (boolean, optional): When true, open the composer, type the message (and attach the photo if given) but DO NOT submit. Returns posted:false, dryRun:true once the publish control is confirmed enabled.
- `imageUrl` (string, optional): Optional photo to attach, fetched from this URL inside the page. The host must be reachable from facebook.com (CSP/CORS) — fbcdn.net image URLs work; for arbitrary images prefer imageBase64.
- `imageBase64` (string, optional): Optional photo to attach, as raw base64 bytes of a JPEG/PNG (no data: prefix). Ignored when imageUrl is set.
- `requireProfile` (boolean, optional): When true, refuse to post if the session is switched to a Page identity (i_user cookie present) — the post would be authored by the Page, and membership/your-content surfaces reflect the Page, not the profile.
- `skipDuplicateCheck` (boolean, optional): Skip the pre-post duplicate guard (the group's my_posted_content page is normally checked for this message first; if already there the script returns alreadyPosted:true without posting).

## Output

- `name` (string | null, optional)
- `dryRun` (boolean, optional): true when the run stopped before submitting because the dryRun arg was set.
- `posted` (boolean, optional): true once the composer dialog closed after submit. false in dryRun and when alreadyPosted.
- `groupId` (string, optional)
- `verified` (boolean, optional): true when the message was found on the group's my_posted_content page right after publishing. false can mean the post is held for admin approval.
- `alreadyPosted` (boolean, optional): true when the duplicate guard found this exact message already on the group's my_posted_content page — nothing was posted.
- `photoAttached` (boolean, optional): true when the photo registered in the composer (blob preview seen) before submit.

## FAQ

### What does "Post to a Facebook group without the Groups API" do?

Publish to Facebook groups from an agent without Graph API group posting permissions, which Meta removed in v19: this acts as the signed-in member, so it needs no app review. Publish a post to a Facebook group, optionally with a photo (imageUrl fetched in-page, or imageBase64). Works on discussion and buy/sell groups. Returns posted, photoAttached, and verified — the post is looked up on the group's "your content" page after publishing, so verified:false flags posts held for admin approval. dryRun arms the composer without publishing.

### How do I automatically post to a Facebook group without the Groups API on facebook.com?

Ask an AI agent connected to Reduck to run reduck/facebook.com/post_to_group, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/post_to_group

### Is there a facebook.com API to post to a Facebook group without the Groups API?

You do not need one. "Post to a Facebook group without the Groups API" drives the real facebook.com pages in a browser, so it works whether or not facebook.com offers an API for this.

### What information do I need to provide?

Required: groupId, message. Optional: dryRun, imageUrl, imageBase64, requireProfile, skipDuplicateCheck.

### What does it return?

It returns name, dryRun, posted, groupId, verified, alreadyPosted, photoAttached.

### Do I need to be logged in to facebook.com?

No. It only uses pages of facebook.com that are reachable without signing in.

### Does it change anything on facebook.com, or only read data?

It makes changes on facebook.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/facebook.com/post_to_group, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/post_to_group

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/facebook.com/post_to_group
