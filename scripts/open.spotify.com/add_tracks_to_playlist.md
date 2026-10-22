# Add tracks to a Spotify playlist

Automatically add tracks to a Spotify playlist on open.spotify.com. Add one or more tracks to the end of a playlist the signed-in Spotify account can edit, in the order given. Spotify accepts duplicates, so a track already in the playlist is added again. Returns the playlist's track count before and after, so the addition can be checked. Use remove_tracks_from_playlist to undo it.

- Site: open.spotify.com
- Address: `reduck/open.spotify.com/add_tracks_to_playlist`
- Updated: 2026-10-21 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/open.spotify.com/add_tracks_to_playlist`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/open.spotify.com/add_tracks_to_playlist
```

## Input

- `tracks` (array, required): Tracks to add, each an id, a spotify:track: uri or an open.spotify.com/track/ link.
- `playlist` (string, required): Target playlist, as an id, a spotify:playlist: uri or an open.spotify.com/playlist/ link. The signed-in account must be able to edit it.

## Output

- `added` (integer, required): How many tracks the playlist gained, read back from Spotify after the addition.
- `requested` (integer, required)
- `playlist_id` (string, required)
- `playlist_name` (string | null, required)
- `track_count_after` (integer, required)
- `track_count_before` (integer, required)
- `track_uris` (array, optional): The tracks sent, as uris, in order.
- `playlist_url` (string, optional)

## FAQ

### What does "Add tracks to a Spotify playlist" do?

Add one or more tracks to the end of a playlist the signed-in Spotify account can edit, in the order given. Spotify accepts duplicates, so a track already in the playlist is added again. Returns the playlist's track count before and after, so the addition can be checked. Use remove_tracks_from_playlist to undo it.

### How do I automatically add tracks to a Spotify playlist on open.spotify.com?

Ask an AI agent connected to Reduck to run reduck/open.spotify.com/add_tracks_to_playlist, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/open.spotify.com/add_tracks_to_playlist

### Is there a open.spotify.com API to add tracks to a Spotify playlist?

You do not need one. "Add tracks to a Spotify playlist" drives the real open.spotify.com pages in a browser, so it works whether or not open.spotify.com offers an API for this.

### What information do I need to provide?

Required: playlist, tracks.

### What does it return?

It returns added, requested, track_uris, playlist_id, playlist_url, playlist_name, track_count_after, track_count_before.

### Do I need to be logged in to open.spotify.com?

Yes. It acts as you on open.spotify.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the open.spotify.com cookies saved by the Reduck extension.

### Does it change anything on open.spotify.com, or only read data?

It makes changes on open.spotify.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/open.spotify.com/add_tracks_to_playlist, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/open.spotify.com/add_tracks_to_playlist

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/open.spotify.com/add_tracks_to_playlist
