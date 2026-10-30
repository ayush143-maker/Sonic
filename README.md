# Sonic

A browser-based music visualiser with visual modes, colour options, track upload, playback controls, and a song list. `Sonicv2.html` is the entry page. A track selected through the upload control is visitor-provided; it is not listed as a repository asset.

## Preview locally

Open `Sonicv2.html` in a browser, or serve the project folder with Python:

```sh
python -m http.server 8000
```

Then visit <http://localhost:8000/Sonicv2.html>.

Browser audio policies may require a direct user action before sound starts.

## Updating the page

Edit visible labels, song-list text, and presentation in `Sonicv2.html`. If you add, move, or rename local assets, update the page's relative references and preserve exact filenames and letter case. The page requests Inter and Space Grotesk from Google Fonts, which requires network access; check fallback typography if those requests fail.

## Configuration and data handling

The repository contains `Sonicv2.html`; no separate configuration file is documented here. Do not put credentials or secrets in tracked files, since browser-delivered values are visible to visitors. Before using a private or sensitive track, review how the page and browser handle the selection; do not assume selected data is private. Visitors' browsers may also request fonts from Google.

## Contributor handoff

Keep changes focused on the page or behavior being updated. Describe what changed and which files were touched when handing off the work. Preserve filenames and relative references, or update references when files move or are renamed. Manually review the page before publishing.

## Review checklist

These are checks to perform, not verified results:

- Review the visualiser, song list, modes, colour options, and controls in a browser at narrow mobile and wide desktop sizes.
- Select a non-sensitive audio file and review selection, playback, pause, and visual response where available. Note the browser and viewport when recording issues.
- Use the keyboard to check access to controls, focus visibility, labels, and interaction order. Check contrast and whether important track or playback state is conveyed in text as well as visually.
- If the visualiser animates, check it with reduced motion enabled and whether animation can be reduced or stopped.