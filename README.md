# Sonic

**Sonic** is a browser-based music visualiser. It combines audio playback with multiple visual modes, colour options, track upload, playback controls, and a song list, letting the listener shape the visual presentation while music plays.

The main entry point is Sonicv2.html. The repository is a static web experience and does not require a package installation step.

## Open locally

Open Sonicv2.html in a modern browser. If you prefer an HTTP preview, run:

    python -m http.server 8000

Then visit the local address shown by the server and open /Sonicv2.html.

## Using local audio

Choose an audio file through the page's upload control and test the playback and visual modes together. Browser audio policies may require a direct user action before sound can start. When changing the visualiser, keep the audio controls accessible and make sure the display remains responsive on mobile screens.
