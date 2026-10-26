# Create a Spotify playlist

Automatically create a Spotify playlist on open.spotify.com. Create a playlist on the signed-in Spotify account, with a name, an optional description, and private (the default) or public. Returns the new playlist's id, uri and link, with the name, description and visibility read back from Spotify after saving. Spotify allows several playlists with one name, so calling it twice creates two. Use delete_playlist to undo it.

- Site: open.spotify.com
- Address: `reduck/open.spotify.com/create_playlist`
- Updated: 2026-10-22 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/open.spotify.com/create_playlist`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/open.spotify.com/create_playlist
```

## Input

- `name` (string, required): Playlist name.
- `private` (boolean, optional): True makes the playlist private, visible only to the account. False leaves it public, as Spotify creates it.
- `description` (string, optional): Playlist description. Empty leaves it blank.

## Output

- `id` (string, required)
- `uri` (string, required)
- `url` (string, required)
- `name` (string, required): Name read back from the saved playlist.
- `public` (boolean, required): Visibility read back from the saved playlist.
- `verified` (boolean, required): Name, description and visibility read back match what was requested.
- `description` (string | null, optional): Description read back from the saved playlist.

## FAQ

### What does "Create a Spotify playlist" do?

Create a playlist on the signed-in Spotify account, with a name, an optional description, and private (the default) or public. Returns the new playlist's id, uri and link, with the name, description and visibility read back from Spotify after saving. Spotify allows several playlists with one name, so calling it twice creates two. Use delete_playlist to undo it.

### How do I automatically create a Spotify playlist on open.spotify.com?

Ask an AI agent connected to Reduck to run reduck/open.spotify.com/create_playlist, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/open.spotify.com/create_playlist

### Is there a open.spotify.com API to create a Spotify playlist?

You do not need one. "Create a Spotify playlist" drives the real open.spotify.com pages in a browser, so it works whether or not open.spotify.com offers an API for this.

### What information do I need to provide?

Required: name. Optional: private, description.

### What does it return?

It returns id, uri, url, name, public, verified, description.

### Do I need to be logged in to open.spotify.com?

Yes. It acts as you on open.spotify.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the open.spotify.com cookies saved by the Reduck extension.

### Does it change anything on open.spotify.com, or only read data?

It makes changes on open.spotify.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/open.spotify.com/create_playlist, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/open.spotify.com/create_playlist

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/open.spotify.com/create_playlist
