# LinkedIn — Create post

Automatically create post on linkedin.com. Publish a text post to your LinkedIn feed, visible to anyone. This creates a real, public post under your account immediately — not a draft or preview. Only plain text posts are supported; images, polls, and articles need a different flow. Requires being logged into LinkedIn. Returns the link to the published post.

- Site: linkedin.com
- Address: `reduck/linkedin.com/create_post`
- Updated: 2026-09-14 (v50)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/create_post`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/create_post
```

## Input

- `text` (string, required): The post body. Plain text; newlines preserved. Any bare URL in the text auto-unfurls into LinkedIn's own link-preview card. Posted publicly ("Anyone") under the logged-in member. Confirm the exact text with the user before running this -- it creates a real, public, immediate post under their account.
- `mentions` (array, optional): Person or organization names to @mention, appended in order at the end of text (each as ' @Name'). Confirm each name with the user before running. If a name is ambiguous (multiple people share it exactly), the run throws listing candidates by headline -- re-run with the name plus enough of their headline/company/org for LinkedIn's own typeahead to narrow to exactly one match (confirmed live this works even though the matched suggestion's displayed name stays just the plain name).
- `imageBase64` (string, optional): A single image to attach, base64-encoded (no data: prefix). Optional. Cannot be combined with scheduleDate/scheduleTime -- LinkedIn's Schedule modal wipes the composer, which would discard the staged image. Multi-image carousels are not yet supported by this script.
- `scheduleDate` (string, optional): Schedule the post instead of publishing immediately: the date to publish, as M/D/YYYY (e.g. "8/25/2026"), in the account's own timezone. Must be provided together with scheduleTime. Must be today or later -- a past date is refused, as is any date LinkedIn's own calendar shows as unavailable (it only allows a limited window into the future). Cannot be combined with imageBase64.
- `scheduleTime` (string, optional): Schedule the post instead of publishing immediately: the time to publish, matching one of LinkedIn's own quarter-hour presets exactly, e.g. "1:00 PM", "11:45 AM". Must be provided together with scheduleDate.
- `imageFilename` (string, optional): Filename for the attached image, e.g. photo.png. Required when imageBase64 is set.
- `imageMimeType` (string, optional): MIME type of the image; inferred from imageFilename's extension when omitted.

## Output

- `url` (string | null, required): Post permalink (resolves to the post); feed it to delete_post or get_post. Null when scheduled (no permalink exists until the post actually goes live).
- `posted` (boolean, required): True once this run's write immediately published a new post. False when scheduled (see `scheduled`), or when an identical post/schedule already existed and nothing new was created (see already_present / alreadyScheduled).
- `shareUrn` (string | null, required): The post's share urn, e.g. urn:li:share:7475847938603192320. On an already_present hit this is the existing post's activity urn instead. Null when scheduled.
- `scheduled` (boolean, required): True if this run scheduled a post (new or already-existing) instead of publishing immediately.
- `account_used` (object, required): The real account the post was published/scheduled under, echoed from the session/UI.
- `scheduledFor` (string | null, required): When scheduled is true, the scheduled-posts panel's own confirmation string, e.g. "Preview of the scheduled post that will be published on Mon August 17, 2026 at 1:00 PM, click to see detail view". Null otherwise.
- `already_present` (boolean, required): True if an immediate post with this exact text was already found on the account's own activity before attempting to publish -- the run stopped there instead of creating a duplicate; url/shareUrn point at that pre-existing post. Never true on a scheduling run (see alreadyScheduled for that case).
- `alreadyScheduled` (boolean, required): True if a scheduled post with this exact text already existed in the account's Scheduled posts queue before this run -- nothing new was scheduled; scheduledFor describes the existing entry. Only meaningful when scheduleDate/scheduleTime were passed.
- `verified_on_page` (boolean, required): True if the script independently reloaded and confirmed the write: for an immediate post, the permalink actually renders the text; for a scheduled post, the Scheduled posts management panel actually lists an entry matching this body; for an already_present/alreadyScheduled hit, this is always true (the existing entry was what was matched).
- `mediaAttached` (boolean | null, optional): True when imageBase64 was provided and the image was confirmed staged (a remove-media control appeared) before publishing. Null when no image was requested.

## FAQ

### What does "LinkedIn — Create post" do?

Publish a text post to your LinkedIn feed, visible to anyone. This creates a real, public post under your account immediately — not a draft or preview. Only plain text posts are supported; images, polls, and articles need a different flow. Requires being logged into LinkedIn. Returns the link to the published post.

### How do I automatically create post on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/create_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/create_post

### Is there a linkedin.com API to create post?

You do not need one. "LinkedIn — Create post" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: text. Optional: mentions, imageBase64, scheduleDate, scheduleTime, imageFilename, imageMimeType.

### What does it return?

It returns url, posted, shareUrn, scheduled, account_used, scheduledFor, mediaAttached, already_present, alreadyScheduled, verified_on_page.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/create_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/create_post

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/create_post
