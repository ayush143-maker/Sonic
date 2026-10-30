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

## Deployment-readiness checklist

The repository lists `Sonicv2.html` as its entry page. The checks below are recommendations to perform before and after publishing; they are not verified deployment results.

- [ ] Confirm the publishing output or root directory is the project directory containing `Sonicv2.html`. This repository does not document a separate build output directory.
- [ ] Confirm the published entry path points to `Sonicv2.html`; do not assume a different default page will open it.
- [ ] Check every local asset reference in `Sonicv2.html`. Keep paths relative to the page, and ensure each referenced file is included at the expected location with matching filename case. No local asset files are listed in the supplied repository inventory.
- [ ] Check that the page still behaves as expected if Google Fonts cannot be reached; the font requests require network access.
- [ ] Keep credentials and secrets out of tracked files. Browser-delivered values are visible to visitors. The repository documents no separate configuration file.
- [ ] After publishing, open the published page at its actual address. Confirm the entry page loads, inspect the browser for missing local resources, and manually review the page and controls there.
- [ ] Repeat the preview after any change to the publishing root, entry page, asset paths, or page configuration.

## Configuration and data handling

The documented repository contents include `Sonicv2.html`; no separate configuration file is documented. Do not put credentials or secrets in tracked files, since browser-delivered values are visible to visitors. Before using a private or sensitive track, review how the page and browser handle the selection; do not assume selected data is private. Visitors' browsers may also request fonts from Google.

## Contributor handoff

Keep changes focused on the page or behavior being updated. Describe what changed and which files were touched when handing off the work. Preserve filenames and relative references, or update references when files move or are renamed. Manually review the page before publishing and perform the post-publishing checks above.

## Review checklist

These are checks to perform, not verified results:

- [ ] Review the visualiser, song list, modes, colour options, and controls in a browser at narrow mobile and wide desktop sizes.
- [ ] Select a non-sensitive audio file and review selection, playback, pause, and visual response where available. Note the browser and viewport when recording issues.
- [ ] Use the keyboard to check access to controls, focus visibility, labels, and interaction order. Check contrast and whether important track or playback state is conveyed in text as well as visually.
- [ ] If the visualiser animates, check it with reduced motion enabled and whether animation can be reduced or stopped.

## Final release review

- Confirm the documented starting point still matches the files present at the repository root.
- Test with network access available and keep a sensible fallback for externally loaded resources.
- Review the published result once on a narrow screen and once on a wider screen; treat this as a release check, not an automated test report.

## Repository map

- `Sonicv2.html` — additional HTML page.
