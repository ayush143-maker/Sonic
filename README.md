# Sonic

Sonic is a browser-based music visualiser. Its page provides visual modes, colour options, track upload, playback controls, and a song list. `Sonicv2.html` is the entry page. Tracks selected through the upload control are visitor-provided, not repository assets.

## Preview locally

Open `Sonicv2.html` in a browser, or serve the project folder with Python:

```sh
python -m http.server 8000
```

Then visit <http://localhost:8000/Sonicv2.html>.

Browser audio policies may require a direct user action before sound starts.

## Editing

Edit visible labels, song-list text, and presentation in `Sonicv2.html`. If local assets are added, moved, or renamed, update their relative references and preserve exact filenames and letter case. The page requests Inter and Space Grotesk from Google Fonts, so those fonts require network access; check the fallback typography if the requests fail.

Review the page in a browser at narrow and wide screen sizes. You can also select a non-sensitive audio file to review selection, playback, pause, and visual response where available. Use the keyboard to check control access, focus visibility, labels, and interaction order. If the visualiser animates, check its behavior with reduced motion enabled.

A selected track should not be assumed private: review how the page and browser handle it before using sensitive audio. Browser-delivered values are visible to visitors; do not put credentials or secrets in tracked files.

## Repository map

- `Sonicv2.html` — page entry point and location for visible copy and presentation.