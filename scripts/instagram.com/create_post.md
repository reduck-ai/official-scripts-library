# Create Instagram post

Automatically create Instagram post on instagram.com. Publish a single-image Instagram feed post from an image URL, inline base64 bytes, or a local file path (image_path, which needs a CLI-run device). Drives the web composer (New post → crop → edit → caption → Share) and returns code, pk, url, caption. Supersedes create_post_from_file.

- Site: instagram.com
- Address: `reduck/instagram.com/create_post`
- Updated: 2026-09-22 (v19)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/create_post`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/create_post
```

## Input

- `caption` (string, optional): Post caption; empty for none. Max 2200 chars.
- `dry_run` (boolean, optional): When true, the whole composer flow runs — the image is attached, cropped, the edit step passed and the caption typed — and then the run stops on the step before Share. Nothing is published, and code/url come back null with dry_run true. Use it to verify an image and caption are accepted without spending a real, irreversible public post.
- `image_url` (string, optional): Direct URL of a single image to post (jpeg/png/gif/webp). Fetched by the browser itself, so it works on devices with no outbound network of their own. No size ceiling and no device requirement. Equivalent to passing a 1-item image_urls.
- `image_path` (string, optional): Path to a single local image file, attached straight from disk by the browser's own low-level file-attach mechanism — no encoding, no size ceiling. Resolved on the machine running the browser, and only works on a device whose browser permits attaching local files directly. An extension-paired browser does not: it refuses with "Not allowed". Absolute paths only. Equivalent to a 1-item images_path.
- `image_urls` (array, optional): 1-10 direct image URLs, in order. A single URL publishes a normal post; 2 or more publish a carousel. Each is fetched by the browser itself, so this works on devices with no outbound network of their own. No size ceiling and no device requirement — the general answer, and the only practical route for a carousel of real photos.
- `images_path` (array, optional): 1-10 paths to local images, in order, attached straight from disk by the browser's own low-level file-attach mechanism. Only works on a device whose browser permits attaching local files directly; an extension-paired browser does not. Absolute paths only. Takes precedence over image_urls.
- `image_base64` (string, optional): A single image's bytes as base64 (a bare payload or a full data: URL), decoded in-page — needs no network and no local file access. Capped at ~96KB of base64, i.e. about a 72KB file. Line-wrapped output, base64url and missing padding are all accepted. Equivalent to a 1-item images_base64.
- `images_base64` (array, optional): 1-10 images as base64 (bare payloads or full data: URLs), in order, decoded in-page. Capped across all images combined at ~96KB of base64 total. Real photos will not fit for more than one — use image_urls for a real carousel. Takes precedence over images_path and image_urls.

## Output

- `url` (string | null, required): Permalink of the new post. Null on a dry run, where nothing was published.
- `code` (string | null, required): Shortcode of the new post. Null on a dry run, where nothing was published.
- `caption_applied` (boolean, required): True when a caption was requested and Instagram recorded it; false when one was requested but the published post carries none. Always true when no caption was requested. Always false on a dry run, where Instagram recorded nothing.
- `pk` (string | null, optional): Media pk. Null on a dry run.
- `caption` (string, optional): The caption Instagram actually recorded on the published post (read back from configure/configure_sidecar), NOT an echo of the input. Empty when none was requested, none landed, or the run was a dry run.
- `dry_run` (boolean, optional): True when this run stopped before Share and published nothing. The image was still attached and the caption still typed — only the final publish was skipped.
- `image_bytes` (number | null, optional): Total size in bytes of the image(s) injected into the composer. null when attached via a *_path field, where the browser opens the file(s) itself and the bytes never cross the driver boundary.
- `carousel_count` (integer | null, optional): carousel_media_count as Instagram reported it on configure_sidecar. null for a single-image post, and null on a dry run.

## FAQ

### What does "Create Instagram post" do?

Publish a single-image Instagram feed post from an image URL, inline base64 bytes, or a local file path (image_path, which needs a CLI-run device). Drives the web composer (New post → crop → edit → caption → Share) and returns code, pk, url, caption. Supersedes create_post_from_file.

### How do I automatically create Instagram post on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/create_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/create_post

### Is there a instagram.com API to create Instagram post?

You do not need one. "Create Instagram post" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Optional: caption, dry_run, image_url, image_path, image_urls, images_path, image_base64, images_base64.

### What does it return?

It returns pk, url, code, caption, dry_run, image_bytes, carousel_count, caption_applied.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It makes changes on instagram.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/create_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/create_post

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/create_post
