# Sonic

A browser-based music visualiser with multiple visual modes, colour options, track upload, playback controls, and a song list. `Sonicv2.html` is the main entry point. Visitors can choose an audio file through the upload control and use the available visual and playback controls. No package installation is required.

## Preview locally

Open `Sonicv2.html` in a browser, or serve the project folder with Python:

    python -m http.server 8000

Then visit http://localhost:8000/Sonicv2.html.

Browser audio policies may require a direct user action before sound starts.

## Browser and platform reliability checklist

These are review steps, not verified results. The repository overview identifies a single HTML page and a Google Fonts request; it does not identify a build system or test suite.

- Review `Sonicv2.html` in current versions of Chrome, Firefox, Safari, and Edge relevant to the intended audience. Include mobile Chrome and mobile Safari if phone use is intended. Record the browser, device or viewport, and any issue found; checking one browser does not establish compatibility in others.
- Inspect the browser console and network panel when loading the page and using its visual and playback controls. Investigate errors, failed requests, and unexpected warnings, including failures to load Google Fonts or local files.
- Check any local file references in `Sonicv2.html` against files present in the repository, verifying relative paths, spelling, and letter case. The uploaded track is selected by the visitor, so it is not expected to be a repository asset.
- Check the Google Fonts request for Inter and Space Grotesk, and whether the page remains legible when the external request is unavailable.
- At narrow mobile and wide desktop sizes, check that the visualiser, song list, upload input, and controls remain visible and usable. Select a non-sensitive audio file and review selection, playback, pause, and the visual response where available. Browser audio policies may require a direct user action.

## Content and asset review checklist

These are review steps, not verified results or measured performance claims:

- Review the visualiser, song list, available modes, colour options, and visible labels for intended content.
- If the page references bundled media, check that each local path resolves and review whether the asset size is appropriate for its use. Replace unnecessarily large assets when practical; remove files only after confirming the page does not use them.
- Treat Google Fonts as an external dependency. Confirm the request is intentional, avoid requesting unused styles, and check readability if it fails.

## Accessibility review checklist

These are future review checks, not claims that accessibility has been verified:

- Navigate `Sonicv2.html` using only the keyboard. Check that the upload input, playback controls, song-list interactions, and visual mode and colour options can be reached and operated.
- Check for a clearly visible focus indicator on each control and confirm that focus order follows the page's task flow.
- Check that playback, upload, mode, and colour controls have meaningful accessible names. Check that track selection and playback state are communicated in text, not only by visual changes.
- Check text, control, and focus-indicator contrast against the page background and within the visualiser. Do not rely on colour alone to distinguish modes or states.
- Review image alternatives in the HTML if images are present. If the visualiser conveys information not otherwise available, consider what text equivalent or status information a user would need.
- Check the visualiser with reduced motion enabled. Review whether animation can be reduced or stopped and whether controls and track information remain usable without motion.

## Personalize the page

Use `Sonicv2.html` to edit visible labels, song-list text, and page presentation. Preserve the Google Fonts links if you want to keep the current typefaces. Keep `Sonicv2.html` at its current location, or update links that point to it if you rename or move it. If you add local assets, keep their paths aligned with their locations relative to the HTML file. Repeat the relevant browser, asset, and accessibility checks after changes.