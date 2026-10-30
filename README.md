# Sonic

A browser-based music visualiser with visual modes, colour options, track upload, playback controls, and a song list. `Sonicv2.html` is the entry page. Visitors can choose an audio file through the upload control; that selected track is not expected to be a repository asset.

## Preview locally

Open `Sonicv2.html` in a browser, or serve the project folder with Python:

```sh
python -m http.server 8000
```

Then visit <http://localhost:8000/Sonicv2.html>.

Browser audio policies may require a direct user action before sound starts.

## Troubleshooting

These are diagnostic steps, not claims of known defects:

1. Confirm that you opened `Sonicv2.html`, the entry page.
2. If page resources fail, inspect local references in the HTML and compare each path, spelling, and letter case with the repository files. Preserve paths relative to the HTML page when moving or renaming assets. A track chosen with the upload control is visitor-selected, not a bundled file.
3. Open browser developer tools and inspect the console and network panel while loading the page and using its controls. Look for failed requests and relevant playback or visualiser errors.
4. The Google Fonts request for Inter and Space Grotesk depends on network access; it is distinct from local files. If it fails, check that fallback typography remains legible. If audio does not start, try an explicit user action and check the browser's playback messages.

## Configuration and data handling

The repository overview lists `Sonicv2.html` and `README.md`, with no separate configuration file documented here. Do not put credentials or secrets in tracked files; browser-delivered values are visible to visitors.

Before using a private or sensitive track, review the page and browser behavior to understand how the selection is handled. Do not assume that selected data is private. The page also requests Google Fonts, so visitors' browsers may contact Google.

## Review checklist

These are checks to perform, not verified results:

- Review the visualiser, song list, modes, colour options, and controls in relevant browsers at narrow mobile and wide desktop sizes.
- Select a non-sensitive audio file and review selection, playback, pause, and visual response where available. Record browser and viewport when noting issues.
- Use the keyboard to check access to controls, focus visibility, labels, and interaction order. Check contrast and whether important track or playback state is conveyed in text as well as visually.
- If the visualiser animates, check it with reduced motion enabled and whether animation can be reduced or stopped.

## Personalize the page

Edit visible labels, song-list text, and presentation in `Sonicv2.html`. Keep the Google Fonts links if you want the current typefaces. Keep the page at its current location unless you update links that point to it. If adding local assets, keep their paths aligned with their locations relative to the HTML file.