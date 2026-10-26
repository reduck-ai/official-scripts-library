# Delete a Spotify playlist

Automatically delete a Spotify playlist on open.spotify.com. Delete a playlist the signed-in Spotify account owns, as the player's Delete action does: it leaves the account's library and its followers can no longer find it. Returns the deleted playlist's id and name. The inverse of create_playlist.

- Site: open.spotify.com
- Address: `reduck/open.spotify.com/delete_playlist`
- Updated: 2026-10-22 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/open.spotify.com/delete_playlist`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/open.spotify.com/delete_playlist
```

## Input

- `playlist` (string, required): Playlist id, spotify:playlist: uri or open.spotify.com/playlist/ link. The signed-in account must own it.

## Output

- `deleted` (boolean, required): True once Spotify confirmed the playlist left the account's library.
- `playlist_id` (string, required)
- `name` (string | null, optional)

## FAQ

### What does "Delete a Spotify playlist" do?

Delete a playlist the signed-in Spotify account owns, as the player's Delete action does: it leaves the account's library and its followers can no longer find it. Returns the deleted playlist's id and name. The inverse of create_playlist.

### How do I automatically delete a Spotify playlist on open.spotify.com?

Ask an AI agent connected to Reduck to run reduck/open.spotify.com/delete_playlist, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/open.spotify.com/delete_playlist

### Is there a open.spotify.com API to delete a Spotify playlist?

You do not need one. "Delete a Spotify playlist" drives the real open.spotify.com pages in a browser, so it works whether or not open.spotify.com offers an API for this.

### What information do I need to provide?

Required: playlist.

### What does it return?

It returns name, deleted, playlist_id.

### Do I need to be logged in to open.spotify.com?

Yes. It acts as you on open.spotify.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the open.spotify.com cookies saved by the Reduck extension.

### Does it change anything on open.spotify.com, or only read data?

It makes changes on open.spotify.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/open.spotify.com/delete_playlist, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/open.spotify.com/delete_playlist

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/open.spotify.com/delete_playlist
