# Sonic

A browser-based music visualiser with multiple visual modes, colour options, track upload, playback controls, and a song list. `Sonicv2.html` is the main entry point. Visitors can choose an audio file through the upload control and use the available visual and playback controls. No package installation is required.

## Preview locally

Open `Sonicv2.html` in a browser, or serve the project folder with Python:

    python -m http.server 8000

Then visit http://localhost:8000/Sonicv2.html. After edits, reload the page and review the affected controls and visual modes.

Browser audio policies may require a direct user action before sound starts.

## Personalize the page

Use `Sonicv2.html` to review and edit the visible labels, song-list text, and page presentation. The page references Google Fonts; preserve those font links if you want to keep the current typefaces. Keep `Sonicv2.html` at its current location, or update any links that point to it if you rename or move it. If you add local assets, keep their paths aligned with their locations relative to the HTML file.