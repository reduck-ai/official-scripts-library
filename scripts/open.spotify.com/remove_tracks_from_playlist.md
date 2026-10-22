# Remove tracks from a Spotify playlist

Automatically remove tracks from a Spotify playlist on open.spotify.com. Remove tracks from a playlist the signed-in Spotify account can edit. Every occurrence of each given track is removed. A track that is not in the playlist is reported in not_found and left alone; if none of them is in it, nothing is changed. Returns the playlist's track count before and after. The inverse of add_tracks_to_playlist.

- Site: open.spotify.com
- Address: `reduck/open.spotify.com/remove_tracks_from_playlist`
- Updated: 2026-10-21 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/open.spotify.com/remove_tracks_from_playlist`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/open.spotify.com/remove_tracks_from_playlist
```

## Input

- `tracks` (array, required): Tracks to remove, each an id, a spotify:track: uri or an open.spotify.com/track/ link.
- `playlist` (string, required): Playlist id, spotify:playlist: uri or open.spotify.com/playlist/ link. The signed-in account must be able to edit it.

## Output

- `removed` (integer, required): How many playlist entries were removed, read back from Spotify after the removal.
- `not_found` (array, required): Requested track uris that were not in the playlist.
- `playlist_id` (string, required)
- `track_count_after` (integer, required)
- `track_count_before` (integer, required)
- `playlist_name` (string | null, optional)

## FAQ

### What does "Remove tracks from a Spotify playlist" do?

Remove tracks from a playlist the signed-in Spotify account can edit. Every occurrence of each given track is removed. A track that is not in the playlist is reported in not_found and left alone; if none of them is in it, nothing is changed. Returns the playlist's track count before and after. The inverse of add_tracks_to_playlist.

### How do I automatically remove tracks from a Spotify playlist on open.spotify.com?

Ask an AI agent connected to Reduck to run reduck/open.spotify.com/remove_tracks_from_playlist, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/open.spotify.com/remove_tracks_from_playlist

### Is there a open.spotify.com API to remove tracks from a Spotify playlist?

You do not need one. "Remove tracks from a Spotify playlist" drives the real open.spotify.com pages in a browser, so it works whether or not open.spotify.com offers an API for this.

### What information do I need to provide?

Required: playlist, tracks.

### What does it return?

It returns removed, not_found, playlist_id, playlist_name, track_count_after, track_count_before.

### Do I need to be logged in to open.spotify.com?

Yes. It acts as you on open.spotify.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the open.spotify.com cookies saved by the Reduck extension.

### Does it change anything on open.spotify.com, or only read data?

It makes changes on open.spotify.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/open.spotify.com/remove_tracks_from_playlist, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/open.spotify.com/remove_tracks_from_playlist

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/open.spotify.com/remove_tracks_from_playlist
