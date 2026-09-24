# WhatsApp — Set group photo

Automatically set group photo on web.whatsapp.com. Set/replace a WhatsApp group's photo (icon) by exact group name. Pass the image as base64 (imageBase64) — it is applied through the group-info photo editor, including the crop/adjust step. Verifies the group photo actually changed before reporting success, and returns the new photoUrl plus replacedExisting. Admin-only; notifies the group. Keep imageBase64 well under ~96KB (MCP payload cap); for larger images serve the file over localhost instead.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/set_group_photo`
- Updated: 2026-09-22 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/set_group_photo`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/set_group_photo
```

## Input

- `group` (string, required): Exact group name, as shown in the chat list
- `mime` (string, optional): Optional MIME type for the imageBase64 route. Default inferred from filename (image/png, image/gif, else image/jpeg).
- `dry_run` (boolean, optional): When true, everything runs — the group opens, the image is staged and WhatsApp's crop dialog accepts it — and then the run stops before the crop is submitted. The photo is not changed and the group is not notified: set comes back false and dry_run true. Reaching that point proves both that the image was accepted and that this account may edit the group, since the dialog opens for neither otherwise.
- `filename` (string, optional): Optional filename to present to WhatsApp for the imageBase64 route. Default group.png
- `attachment` (string, optional): The group photo, bound through the platform's own file channel and handed straight to the group drawer's file input. Preferred over imageBase64: it carries the bytes outside the argument payload, so it is not subject to the ~96KB cap and a normal-sized photo needs no shrinking or localhost server. Provide this or imageBase64. WhatsApp requires at least 192x192 pixels.
- `imageBase64` (string, optional): The image bytes, base64-encoded (jpg/png/gif), as an alternative to the `attachment` input. Keep it well under ~96KB of base64 — the MCP transport caps the payload. Provide this or attachment. WhatsApp requires at least 192x192 pixels.

## Output

- `set` (boolean, required): False on a dry run, where the photo was not changed.
- `group` (string, required)
- `dry_run` (boolean, optional): True when this run stopped before submitting the crop. The image was still staged and accepted by WhatsApp's crop dialog — only the submit was skipped.
- `photoUrl` (string | null, optional): The URL of the group photo after the change. On a dry run this is the photo the group had BEFORE, since nothing was changed — null when it had none.
- `replacedExisting` (boolean, optional): true if the group already had a photo that was replaced. On a dry run, whether one WOULD have been replaced.

## FAQ

### What does "WhatsApp — Set group photo" do?

Set/replace a WhatsApp group's photo (icon) by exact group name. Pass the image as base64 (imageBase64) — it is applied through the group-info photo editor, including the crop/adjust step. Verifies the group photo actually changed before reporting success, and returns the new photoUrl plus replacedExisting. Admin-only; notifies the group. Keep imageBase64 well under ~96KB (MCP payload cap); for larger images serve the file over localhost instead.

### How do I automatically set group photo on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/set_group_photo, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/set_group_photo

### Is there a web.whatsapp.com API to set group photo?

You do not need one. "WhatsApp — Set group photo" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: group. Optional: mime, dry_run, filename, attachment, imageBase64.

### What does it return?

It returns set, group, dry_run, photoUrl, replacedExisting.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It makes changes on web.whatsapp.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/set_group_photo, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/set_group_photo

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/set_group_photo
