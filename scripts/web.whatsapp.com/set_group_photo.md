# WhatsApp — Set group photo

Automatically set group photo on web.whatsapp.com. Set/replace a WhatsApp group's photo (icon) by exact group name. Pass the image as base64 (imageBase64) — it is applied through the group-info photo editor, including the crop/adjust step. Verifies the group photo actually changed before reporting success, and returns the new photoUrl plus replacedExisting. Admin-only; notifies the group. Keep imageBase64 well under ~96KB (MCP payload cap); for larger images serve the file over localhost instead.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/set_group_photo`
- Updated: 2026-08-31 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/set_group_photo`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/set_group_photo
```

## Input

- `group` (string, required): Exact group name, as shown in the chat list
- `imageBase64` (string, required): The image bytes, base64-encoded (jpg/png/gif). Keep it well under ~96KB of base64 - the MCP transport caps the payload.
- `mime` (string, optional): Optional MIME type. Default inferred from filename (image/png, image/gif, else image/jpeg).
- `filename` (string, optional): Optional filename to present to WhatsApp. Default group.png

## Output

- `set` (boolean, required)
- `group` (string, required)
- `photoUrl` (string, optional): The URL of the group photo after the change
- `replacedExisting` (boolean, optional): true if the group already had a photo that was replaced

## FAQ

### What does "WhatsApp — Set group photo" do?

Set/replace a WhatsApp group's photo (icon) by exact group name. Pass the image as base64 (imageBase64) — it is applied through the group-info photo editor, including the crop/adjust step. Verifies the group photo actually changed before reporting success, and returns the new photoUrl plus replacedExisting. Admin-only; notifies the group. Keep imageBase64 well under ~96KB (MCP payload cap); for larger images serve the file over localhost instead.

### How do I automatically set group photo on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/set_group_photo, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/set_group_photo

### Is there a web.whatsapp.com API to set group photo?

You do not need one. "WhatsApp — Set group photo" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: group, imageBase64. Optional: mime, filename.

### What does it return?

It returns set, group, photoUrl, replacedExisting.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It makes changes on web.whatsapp.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/set_group_photo, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/set_group_photo

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/set_group_photo
