# Get tracks of a Spotify playlist

Automatically get tracks of a Spotify playlist on open.spotify.com. Read one page of 25 tracks of a Spotify playlist, or of your Liked Songs, as the signed-in user: the playlist uri and name, its total track count, and for each track its position, uri, name, artists, album, duration, play count and when and by whom it was added. Pass offset to read the next pages; next_offset is null after the last page. An empty playlist returns no tracks.

- Site: open.spotify.com
- Address: `reduck/open.spotify.com/get_playlist_tracks`
- Updated: 2026-10-21 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/open.spotify.com/get_playlist_tracks`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/open.spotify.com/get_playlist_tracks
```

## Input

- `playlist` (string, required): Playlist id, spotify:playlist: uri or open.spotify.com/playlist/ link, or "liked" for the signed-in user's Liked Songs.
- `offset` (integer, optional): Position of the first track to return, zero-based. Spotify serves 25 tracks per page: pass the previous answer's next_offset.

## Output

- `uri` (string, required)
- `offset` (integer, required)
- `tracks` (array, required)
- `total_count` (integer, required)
- `name` (string | null, optional)
- `next_offset` (integer | null, optional): Offset of the next page, or null after the last one.

## FAQ

### What does "Get tracks of a Spotify playlist" do?

Read one page of 25 tracks of a Spotify playlist, or of your Liked Songs, as the signed-in user: the playlist uri and name, its total track count, and for each track its position, uri, name, artists, album, duration, play count and when and by whom it was added. Pass offset to read the next pages; next_offset is null after the last page. An empty playlist returns no tracks.

### How do I automatically get tracks of a Spotify playlist on open.spotify.com?

Ask an AI agent connected to Reduck to run reduck/open.spotify.com/get_playlist_tracks, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/open.spotify.com/get_playlist_tracks

### Is there a open.spotify.com API to get tracks of a Spotify playlist?

You do not need one. "Get tracks of a Spotify playlist" drives the real open.spotify.com pages in a browser, so it works whether or not open.spotify.com offers an API for this.

### What information do I need to provide?

Required: playlist. Optional: offset.

### What does it return?

It returns uri, name, offset, tracks, next_offset, total_count.

### Do I need to be logged in to open.spotify.com?

Yes. It acts as you on open.spotify.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the open.spotify.com cookies saved by the Reduck extension.

### Does it change anything on open.spotify.com, or only read data?

It only reads. It looks things up on open.spotify.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/open.spotify.com/get_playlist_tracks, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/open.spotify.com/get_playlist_tracks

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/open.spotify.com/get_playlist_tracks
