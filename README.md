# Sonic

Sonic is a browser-based music visualiser. `Sonicv2.html` is the entry page, with audio playback, a song list, selectable visual modes, and colour themes.

## Preview locally

Open `Sonicv2.html` in a browser, or serve the project folder with Python:

```sh
python -m http.server 8000
```

Then visit <http://localhost:8000/Sonicv2.html>. Audio may require a direct user action before playback, depending on browser policy.

## Add and play tracks

Choose files with the upload control or drop them on the visualiser. The handler accepts filenames ending in MP3, WAV, M4A, OGG, FLAC, or WEBM; unsupported extensions are skipped with a toast. The page derives each track title from its filename. The Songs panel shows tracks and durations: select a track to play it, or use its delete control to remove it.

Playback controls include play/pause, previous, next, shuffle, repeat, and a clickable progress bar for seeking. Space toggles playback, the left and right arrow keys move between tracks, and F toggles fullscreen. Repeat replays the current song when it ends. Without repeat, playback advances; with shuffle on, previous, next, and automatic advancement choose a random track.

Choose among Wave Mesh, Oscilloscope, Frequency Bars, Particles, and Fourier Wave visualisations, and Emerald, Azure, or Blush themes. The visualiser uses a Web Audio API analyser connected to the audio element and speakers to read frequency and time-domain data.

## Track storage and limits

Tracks and metadata are saved in IndexedDB, in database `SonicDB4` and object store `tracks`. On startup, records older than 24 hours are deleted and the remaining tracks are loaded. Deleting a track from the Songs panel also deletes its stored record. This is browser-local storage, not a server library; browser storage quotas and user-cleared site data can affect availability.

If IndexedDB initialization fails, the page shows “Storage unavailable. Using memory only.” However, adding tracks still calls the IndexedDB write function; the source does not provide a separate in-memory upload path. Treat that warning as a limitation, not a guarantee that uploads will work without IndexedDB.

## Editing

Edit visible labels and presentation in `Sonicv2.html`. Inter and Space Grotesk load from Google Fonts, so typography may fall back when offline. Review file selection, playback, deletion, keyboard controls, and visual response in a browser; avoid sensitive audio when testing.